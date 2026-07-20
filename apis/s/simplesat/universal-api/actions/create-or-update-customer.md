# Simplesat: Create or Update Customer

Creates or updates a customer in Simplesat.

```
POST https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no |  |
| `email` | string | no |  |
| `name` | string | no |  |
| `company` | string | no |  |
| `tags[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customAttributes` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "custom_attributes": {},
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
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
| `custom_attributes` | object |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Simplesat API, this operation is `POST /api/v1/customers` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

