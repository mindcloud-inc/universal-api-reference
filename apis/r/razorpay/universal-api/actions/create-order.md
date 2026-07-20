# Razorpay: Create Order

Creates a new order in Razorpay.

```
POST https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Order amount in the smallest currency subunit. |
| `currency` | string | yes | ISO currency code (for example INR). |
| `receipt` | string | no |  |
| `notes` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountDue": 1,
      "amountPaid": 1,
      "attempts": 1,
      "createdAt": 1,
      "currency": "string",
      "entity": "string",
      "id": "string",
      "notes": {
        "source": "string"
      },
      "offerId": {},
      "receipt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountDue` | number |  |
| `amountPaid` | number |  |
| `attempts` | number |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `entity` | string |  |
| `id` | string |  |
| `notes` | object |  |
| `notes.source` | string |  |
| `offerId` | object |  |
| `receipt` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `POST /v1/orders` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

