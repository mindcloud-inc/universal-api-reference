# Fintoc: Create Payment Link

Creates a payment link in Fintoc.

```
POST https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "1000",
  "currency": "MXN"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "1000",
    "currency": "MXN"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount in minor units for the payment link. Example: `1000`. |
| `currency` | string | yes | ISO currency code. This test account accepts MXN. Example: `MXN`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "checkout": {},
      "created_at": "string",
      "currency": "string",
      "customer_email": "ava@example.com",
      "expires_at": "string",
      "id": "string",
      "metadata": {},
      "mode": "string",
      "object": "string",
      "recipient_account": {},
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `checkout` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer_email` | string |  |
| `expires_at` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `object` | string |  |
| `recipient_account` | object |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `POST /v1/payment_links` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-link.md) for the provider-specific parameters and requirements.

