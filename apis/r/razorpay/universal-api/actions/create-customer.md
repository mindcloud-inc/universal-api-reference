# Razorpay: Create Customer

Creates a new customer in Razorpay.

```
POST https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-customer', {
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
| `name` | string | no |  |
| `contact` | string | no |  |
| `email` | string | no |  |
| `failExisting` | string | no |  |
| `gstin` | string | no |  |
| `notes` | object | no |  |

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

Through the native Razorpay API, this operation is `POST /v1/customers` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

