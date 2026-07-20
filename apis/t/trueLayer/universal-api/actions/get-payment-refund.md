# TrueLayer: Get Payment Refund

Retrieves a payment refund from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-refund?connectionId=$CONNECTION_ID&payment_id=string&refund_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payment_id": "string",
  "refund_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-payment-refund?${params}`, {
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
| `payment_id` | string | yes | TrueLayer payment ID. |
| `refund_id` | string | yes | TrueLayer refund ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_in_minor": 1,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_in_minor` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/payments/:payment_id/refunds/:refund_id` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-refund.md) for the provider-specific parameters and requirements.

