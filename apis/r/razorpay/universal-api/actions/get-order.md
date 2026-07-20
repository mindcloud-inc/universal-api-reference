# Razorpay: Get Order

Retrieves an order from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the order. |

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
      "checkout": {},
      "createdAt": 1,
      "currency": "string",
      "description": {},
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
| `checkout` | object |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `description` | object |  |
| `entity` | string |  |
| `id` | string |  |
| `notes` | object |  |
| `notes.source` | string |  |
| `offerId` | object |  |
| `receipt` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/orders/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

