# Fintoc: Get Payment Intent

Retrieves a payment intent from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/get-payment-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/get-payment-intent?connectionId=$CONNECTION_ID&id=pi_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "pi_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/get-payment-intent?${params}`, {
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
| `id` | string | yes | Payment intent identifier. Example: `pi_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "recipient_account": {},
      "reference_id": "string",
      "sender_account": {},
      "status": "string",
      "transaction_date": "string",
      "widget_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `recipient_account` | object |  |
| `reference_id` | string |  |
| `sender_account` | object |  |
| `status` | string |  |
| `transaction_date` | string |  |
| `widget_token` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v1/payment_intents/:id` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-intent.md) for the provider-specific parameters and requirements.

