# BigCommerce (B2B): Update Invoice



```
POST https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/update-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `details.details.lineItems[]` | array | no |  |
| `details.details.lineItems[].sku` | string | no |  |
| `details.details.lineItems[].unitPrice.code` | string | no |  |
| `dueDate` | number | no |  |
| `originalBalance.code` | string | no |  |
| `details.details` | object | no |  |
| `details.details.lineItems[].quantity` | string | no |  |
| `details.details.lineItems[].unitPrice.value` | string | no |  |
| `openBalance.code` | string | no |  |
| `openBalance.value` | number | no |  |
| `originalBalance.value` | number | no |  |
| `status` | number | no |  |
| `details.details.lineItems[].unitPrice` | object | no |  |
| `openBalance` | object | no |  |
| `details.details.lineItems[].description` | string | no |  |
| `originalBalance` | object | no |  |
| `details` | object | no |  |
| `details.details.lineItems[].comments` | string | no |  |
| `customerId` | string | no |  |
| `invoiceId` | string | yes |  |
| `purchaseOrderNumber` | string | no |  |
| `externalPdfUrl` | string | no |  |
| `termsConditions` | string | no |  |
| `externalId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce (B2B) API returns.

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `PUT ip/invoices/:invoiceId` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

