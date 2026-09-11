# BigCommerce (B2B): Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dueDate` | number | no |  |
| `externalId` | string | no |  |
| `invoiceNumber` | string | yes |  |
| `termsConditions` | string | no |  |
| `details.details.lineItems[]` | array | no |  |
| `details.details.lineItems[].sku` | string | no |  |
| `details.details.lineItems[].unitPrice.code` | string | no |  |
| `extraFields[].fieldName` | string | no |  |
| `status` | number | no |  |
| `details.details` | object | no |  |
| `details.details.lineItems[].quantity` | string | no |  |
| `details.details.lineItems[].unitPrice.value` | string | no |  |
| `openBalance.code` | string | no |  |
| `openBalance.value` | number | no |  |
| `originalBalance` | object | no |  |
| `originalBalance.code` | string | no |  |
| `originalBalance.value` | number | no |  |
| `details.details.lineItems[].unitPrice` | object | no |  |
| `openBalance` | object | no |  |
| `details.details.lineItems[].description` | string | no |  |
| `issuedAt` | number | no |  |
| `details` | object | no |  |
| `details.details.lineItems[].comments` | string | no |  |
| `customerId` | string | no |  |
| `purchaseOrderNumber` | string | no |  |
| `extraFields[]` | array | no |  |
| `externalPdfUrl` | string | no |  |
| `orderNumber` | string | no | BigCommerce order ID associated with this invoice. |
| `extraFields[].fieldValue` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce (B2B) API returns.

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `POST ip/invoices` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

