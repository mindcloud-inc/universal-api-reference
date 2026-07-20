# Retently: Upsert Customers

Creates or updates customers in Retently.

```
PUT https://connect.mindcloud.co/v1/universal/retently/latest/actions/upsert-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retently/latest/actions/upsert-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscribers[]": [
    "string"
  ],
  "subscribers[].email": "ava@example.com",
  "subscribers[].properties[].label": "string",
  "subscribers[].properties[].type": "string",
  "subscribers[].properties[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/upsert-customers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscribers[]": ["string"],
    "subscribers[].email": "ava@example.com",
    "subscribers[].properties[].label": "string",
    "subscribers[].properties[].type": "string",
    "subscribers[].properties[].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscribers[]` | array<string> | yes | An array of customers |
| `subscribers[].email` | string | yes | Email address |
| `subscribers[].firstName` | string | no | First name |
| `subscribers[].lastName` | string | no | Last name |
| `subscribers[].company` | string | no | Company name |
| `subscribers[].tags[]` | array<string> | no | An array of tags. Example: [âfooâ, âbarâ, âbazâ] |
| `subscribers[].properties[]` | array<object> | no | Customer properties to create or update. |
| `subscribers[].properties[].label` | string | yes | Property label |
| `subscribers[].properties[].type` | string | yes | Property type |
| `subscribers[].properties[].value` | string | yes | Property value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "properties": [
        {}
      ],
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `properties` | array<object> |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `POST /api/v2/customers` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-customers.md) for the provider-specific parameters and requirements.

