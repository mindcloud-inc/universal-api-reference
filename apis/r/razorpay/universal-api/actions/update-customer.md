# Razorpay: Update Customer

Updates an existing customer in Razorpay.

```
PUT https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the customer. |
| `name` | string | no |  |
| `contact` | string | no |  |
| `email` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "entity": "string",
      "gstin": {},
      "id": "string",
      "name": "Ava Chen",
      "notes": {
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `entity` | string |  |
| `gstin` | object |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | object |  |
| `notes.source` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `PUT /v1/customers/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

