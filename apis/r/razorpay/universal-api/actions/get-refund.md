# Razorpay: Get Refund

Retrieves a refund from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-refund?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-refund?${params}`, {
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
| `id` | string | yes | Unique identifier of the refund. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquirerData": {},
      "amount": 1,
      "batchId": "string",
      "createdAt": 1,
      "currency": "string",
      "entity": "string",
      "id": "string",
      "notes": {},
      "paymentId": "string",
      "receipt": "string",
      "speedProcessed": "string",
      "speedRequested": "string",
      "status": "string"
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
| `batchId` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `entity` | string |  |
| `id` | string |  |
| `notes` | object |  |
| `paymentId` | string |  |
| `receipt` | string |  |
| `speedProcessed` | string |  |
| `speedRequested` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/refunds/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-refund.md) for the provider-specific parameters and requirements.

