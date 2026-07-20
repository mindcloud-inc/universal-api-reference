# PayTabs: Create Hosted Payment Page with Invoice



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-hosted-payment-page-with-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-hosted-payment-page-with-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tran_type": "sale",
  "tran_class": "ecom",
  "cart_currency": "string",
  "cart_amount": 1,
  "cart_id": "string",
  "cart_description": "string",
  "invoice": {},
  "callback": "https://mindcloud.co",
  "return": "https://mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-hosted-payment-page-with-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tran_type": "sale",
    "tran_class": "ecom",
    "cart_currency": "string",
    "cart_amount": 1,
    "cart_id": "string",
    "cart_description": "string",
    "invoice": {},
    "callback": "https://mindcloud.co",
    "return": "https://mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tran_type` | string | yes | PayTabs transaction type, usually sale. Default: `sale`. |
| `tran_class` | string | yes | PayTabs transaction class, usually ecom. Default: `ecom`. |
| `cart_currency` | string | yes | Payment currency. |
| `cart_amount` | number | yes | Payment amount. |
| `cart_id` | string | yes | Unique merchant cart ID. |
| `cart_description` | string | yes | Cart description. |
| `invoice` | object | yes | Invoice object with at least line_items. |
| `callback` | string | yes | Callback URL. Default: `https://mindcloud.co`. |
| `return` | string | yes | Return URL. Default: `https://mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceId": "string",
      "message": "string",
      "redirectUrl": "https://example.com",
      "tranRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceId` | string |  |
| `message` | string |  |
| `redirectUrl` | string |  |
| `tranRef` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hosted-payment-page-with-invoice.md) for the provider-specific parameters and requirements.

