# Razorpay: Get Payment

Retrieves a payment from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-payment?${params}`, {
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
| `id` | string | yes | Unique identifier of the payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquirerData": {},
      "amount": 1,
      "amountRefunded": 1,
      "captured": true,
      "cardId": "string",
      "contact": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "email": "ava@example.com",
      "entity": "string",
      "errorCode": "string",
      "errorDescription": "string",
      "errorReason": "string",
      "errorSource": "string",
      "errorStep": "string",
      "fee": 1,
      "id": "string",
      "international": true,
      "method": "string",
      "notes": {},
      "orderId": "string",
      "refundStatus": "string",
      "status": "string",
      "tax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquirerData` | object |  |
| `amount` | number |  |
| `amountRefunded` | number |  |
| `captured` | boolean |  |
| `cardId` | string |  |
| `contact` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `email` | string |  |
| `entity` | string |  |
| `errorCode` | string |  |
| `errorDescription` | string |  |
| `errorReason` | string |  |
| `errorSource` | string |  |
| `errorStep` | string |  |
| `fee` | number |  |
| `id` | string |  |
| `international` | boolean |  |
| `method` | string |  |
| `notes` | object |  |
| `orderId` | string |  |
| `refundStatus` | string |  |
| `status` | string |  |
| `tax` | number |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/payments/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.

