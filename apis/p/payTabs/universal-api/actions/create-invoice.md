# PayTabs: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-invoice" \
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
  "hide_shipping": "true",
  "customer_ref": "string",
  "customer_details": {},
  "invoice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-invoice', {
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
    "hide_shipping": "true",
    "customer_ref": "string",
    "customer_details": {},
    "invoice": {}
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
| `cart_currency` | string | yes | Invoice cart currency, for example AED. |
| `cart_amount` | number | yes | Invoice cart amount. |
| `cart_id` | string | yes | Unique merchant cart ID. |
| `cart_description` | string | yes | Invoice/cart description. |
| `hide_shipping` | boolean | yes | Whether to hide shipping details. Default: `true`. |
| `customer_ref` | string | yes | Customer reference. |
| `customer_details` | object | yes | Customer details object. |
| `invoice` | object | yes | Invoice details object including line items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "customerDetails": {},
      "invoice": {},
      "invoiceId": "string",
      "invoiceStatus": "string",
      "invoiceUrl": "https://example.com",
      "message": "string",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `customerDetails` | object |  |
| `invoice` | object |  |
| `invoiceId` | string |  |
| `invoiceStatus` | string |  |
| `invoiceUrl` | string |  |
| `message` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/new/invoice` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

