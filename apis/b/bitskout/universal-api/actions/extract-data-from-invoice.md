# Bitskout: Extract Data from Invoice

Extracts invoice data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | no | Download URL for the invoice file to extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "CURRENCY": "string",
        "CUSTOMER_ADDRESS": "string",
        "CUSTOMER_NAME": "Ava Chen",
        "DISCOUNT": "string",
        "DUE_DATE": "string",
        "INVOICE_RECEIPT_DATE": "string",
        "INVOICE_RECEIPT_ID": "string",
        "LINE_ITEMS": "string",
        "name": "Ava Chen",
        "NUMBER_OF_PAGES": 1,
        "RawJSON": "string",
        "RECEIVER_ADDRESS": "string",
        "SUBTOTAL": "string",
        "SUPPLIER_ADDRESS": "string",
        "TAX": "string",
        "TOTAL": "string",
        "VENDOR_NAME": "Ava Chen",
        "VENDOR_VAT_NUMBER": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Invoice extraction outputs |
| `outputs.CURRENCY` | string | Currency |
| `outputs.CUSTOMER_ADDRESS` | string | Customer's Address |
| `outputs.CUSTOMER_NAME` | string | Customer's Name |
| `outputs.DISCOUNT` | string | Discount |
| `outputs.DUE_DATE` | string | Due Date |
| `outputs.INVOICE_RECEIPT_DATE` | string | Invoice Receipt Date |
| `outputs.INVOICE_RECEIPT_ID` | string | Invoice Receipt ID |
| `outputs.LINE_ITEMS` | string | Line Items as CSV |
| `outputs.name` | string | File Name |
| `outputs.NUMBER_OF_PAGES` | number | Number of pages in the document |
| `outputs.RawJSON` | string | Raw JSON |
| `outputs.RECEIVER_ADDRESS` | string | Receiver's Address |
| `outputs.SUBTOTAL` | string | Subtotal |
| `outputs.SUPPLIER_ADDRESS` | string | Supplier Address |
| `outputs.TAX` | string | Tax |
| `outputs.TOTAL` | string | Total |
| `outputs.VENDOR_NAME` | string | Vendor's name |
| `outputs.VENDOR_VAT_NUMBER` | string | Vendor's VAT Number |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/invoices` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-invoice.md) for the provider-specific parameters and requirements.

