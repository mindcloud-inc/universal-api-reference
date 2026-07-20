# TrueLayer: Create Payment Refund

Creates a payment refund in TrueLayer.

```
POST https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payment-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payment-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payment-refund', {
  method: 'POST',
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
| `id` | string | yes | TrueLayer payment ID. |

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

Through the native TrueLayer API, this operation is `POST /v3/payments/:id/refunds` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-refund.md) for the provider-specific parameters and requirements.

