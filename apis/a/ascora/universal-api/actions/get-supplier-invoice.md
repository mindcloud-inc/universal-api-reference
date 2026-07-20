# Ascora: Get Supplier Invoice

Retrieves a supplier invoice from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-supplier-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-supplier-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-supplier-invoice?${params}`, {
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
| `id` | string | yes | Supplier Invoice ID. |

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
            "isTaxable": true,
            "partNumber": "string",
            "quantity": 1,
            "reference": "string",
            "totalAmountExTax": 1,
            "totalAmountIncTax": 1,
            "unitCostExTax": 1
          }
        ],
        "sentToAccounts": true,
        "supplier": {
          "id": "string",
          "name": "Ava Chen"
        },
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
| `supplierInvoice.lines[].isTaxable` | boolean |  |
| `supplierInvoice.lines[].partNumber` | string |  |
| `supplierInvoice.lines[].quantity` | number |  |
| `supplierInvoice.lines[].reference` | string |  |
| `supplierInvoice.lines[].totalAmountExTax` | number |  |
| `supplierInvoice.lines[].totalAmountIncTax` | number |  |
| `supplierInvoice.lines[].unitCostExTax` | number |  |
| `supplierInvoice.sentToAccounts` | boolean |  |
| `supplierInvoice.supplier.id` | string |  |
| `supplierInvoice.supplier.name` | string |  |
| `supplierInvoice.supplierInvoiceId` | string |  |
| `supplierInvoice.totalAmountExTax` | number |  |
| `supplierInvoice.totalAmountIncTax` | number |  |
| `supplierInvoice.trackingNumber` | string |  |
| `supplierInvoice.type` | string |  |

## Native endpoint

Through the native Ascora API, this operation is `GET /SupplierInvoices/SupplierInvoice/{{id}}` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier-invoice.md) for the provider-specific parameters and requirements.

