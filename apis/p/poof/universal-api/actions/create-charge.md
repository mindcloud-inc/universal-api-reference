# Poof: Create Charge

Creates a new fiat charge in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "15",
  "payment": "paypal",
  "currency": "usd",
  "redirect_url": "https://www.poof.io",
  "success_url": "https://www.poof.io/success"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-charge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "15",
    "payment": "paypal",
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
| `amount` | string | yes | Charge amount. Default: `15`. |
| `payment` | string | yes | Fiat payment method; docs example uses paypal. Default: `paypal`. |
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
      "paymentLink": "https://example.com",
      "qrCode": "string",
      "trackingId": "string"
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
| `qrCode` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/create_fiat_charge` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-charge.md) for the provider-specific parameters and requirements.

