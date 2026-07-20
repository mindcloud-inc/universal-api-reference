# Poof: Create Invoice

Creates a new fiat invoice in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "15",
  "payment": "cashapp",
  "currency": "usd",
  "redirect_url": "https://www.poof.io",
  "success_url": "https://www.poof.io/success"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "15",
    "payment": "cashapp",
    "currency": "usd",
    "redirect_url": "https://www.poof.io",
    "success_url": "https://www.poof.io/success"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | string | yes | Invoice amount. Default: `15`. |
| `payment` | string | yes | Fiat payment method. Default: `cashapp`. |
| `currency` | string | yes | Fiat currency code. Default: `usd`. |
| `redirect_url` | string | yes | Redirect URL. Default: `https://www.poof.io`. |
| `success_url` | string | yes | Success URL. Default: `https://www.poof.io/success`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "currency": "string",
      "payment": "string",
      "paymentLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `currency` | string |  |
| `payment` | string |  |
| `paymentLink` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/create_fiat_invoice` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

