# Ascora: Create Supplier Invoice

Creates a new supplier invoice in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingNumber": "SUP-20260324-001",
  "invoiceDate": "2026-03-24",
  "dueDate": "2026-04-24",
  "supplier.name": "Codex Stage3 Supplier 202603241835",
  "lines[].description": "PVC fittings",
  "lines[].quantity": "1",
  "lines[].totalAmountExTax": "50"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-supplier-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingNumber": "SUP-20260324-001",
    "invoiceDate": "2026-03-24",
    "dueDate": "2026-04-24",
    "supplier.name": "Codex Stage3 Supplier 202603241835",
    "lines[].description": "PVC fittings",
    "lines[].quantity": "1",
    "lines[].totalAmountExTax": "50"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingNumber` | string | yes | Supplier invoice number or credit note number. Example: `SUP-20260324-001`. |
| `invoiceDate` | date | yes | Date associated with the supplier invoice. Example: `2026-03-24`. |
| `dueDate` | date | yes | Date on which the supplier invoice is due. Example: `2026-04-24`. |
| `supplier.name` | string | yes | Name of the supplier linked to the invoice. Example: `Codex Stage3 Supplier 202603241835`. |
| `lines[].description` | string | yes | Description for a supplier invoice line. Example: `PVC fittings`. |
| `lines[].partNumber` | string | no | Part number for a supplier invoice line. Example: `CLI123`. |
| `lines[].quantity` | number | yes | Quantity for a supplier invoice line. Example: `1`. |
| `lines[].totalAmountExTax` | number | yes | Total ex-tax amount for a supplier invoice line. Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | no | Purchase order or job number associated with the supplier invoice. Example: `PO-12345`. |
| `type` | string | no | Use INVOICE to create a supplier invoice or CREDIT to create a credit note. Example: `INVOICE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "supplierInvoice": {
        "accepted": true,
        "accountCode": "string",
        "createdOn": "2026-05-07T12:00:00.000Z",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "isExpense": true,
        "lines": [
          {
            "accountCode": "string",
            "description": "string",
            "partNumber": "string",
            "quantity": 1,
            "reference": "string",
            "totalAmountExTax": 1,
            "totalAmountIncTax": 1,
            "unitCostExTax": 1
          }
        ],
        "reference": "string",
        "sentToAccounts": true,
        "supplierInvoiceId": "string",
        "totalAmountExTax": 1,
        "totalAmountIncTax": 1,
        "trackingNumber": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `supplierInvoice.accepted` | boolean |  |
| `supplierInvoice.accountCode` | string |  |
| `supplierInvoice.createdOn` | date |  |
| `supplierInvoice.dueDate` | date |  |
| `supplierInvoice.invoiceDate` | date |  |
| `supplierInvoice.isExpense` | boolean |  |
| `supplierInvoice.lines[].accountCode` | string |  |
| `supplierInvoice.lines[].description` | string |  |
| `supplierInvoice.lines[].partNumber` | string |  |
| `supplierInvoice.lines[].quantity` | number |  |
| `supplierInvoice.lines[].reference` | string |  |
| `supplierInvoice.lines[].totalAmountExTax` | number |  |
| `supplierInvoice.lines[].totalAmountIncTax` | number |  |
| `supplierInvoice.lines[].unitCostExTax` | number |  |
| `supplierInvoice.reference` | string |  |
| `supplierInvoice.sentToAccounts` | boolean |  |
| `supplierInvoice.supplierInvoiceId` | string |  |
| `supplierInvoice.totalAmountExTax` | number |  |
| `supplierInvoice.totalAmountIncTax` | number |  |
| `supplierInvoice.trackingNumber` | string |  |
| `supplierInvoice.type` | string |  |

## Native endpoint

Through the native Ascora API, this operation is `POST /SupplierInvoices/SupplierInvoice` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier-invoice.md) for the provider-specific parameters and requirements.

