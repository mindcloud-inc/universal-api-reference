# Simplesat: Update Customer

Updates an existing customer in Simplesat.

```
PUT https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no |  |
| `name` | string | no |  |
| `company` | string | no |  |
| `tags[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The ID of the customer to update |
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

Through the native Simplesat API, this operation is `PUT /api/v1/customers/:customer_id` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

