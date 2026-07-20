# Ascora: List Supplier Invoices

Retrieves supplier invoices from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplier-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplier-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplier-invoices?${params}`, {
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
| `invoiceDateEnd` | date | no | Search for invoices with an Invoice Date on or before the specified date. |
| `invoiceDateStart` | date | no | Search for invoices with an Invoice Date on or after the specified date. |
| `supplierName` | string | no | Performs a partial match against the Supplier Name. |
| `toBeSentToAccounting` | boolean | no | Limits the results returned to only Supplier Invoices that have not been pushed to the Accounting Package yet. |
| `trackingNumber` | string | no | Performs a partial match against the Supplier Invoice/Credit Note Number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
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
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].accepted` | boolean |  |
| `results[].accountCode` | string |  |
| `results[].createdOn` | date |  |
| `results[].dueDate` | date |  |
| `results[].invoiceDate` | date |  |
| `results[].isExpense` | boolean |  |
| `results[].lines[].accountCode` | string |  |
| `results[].lines[].description` | string |  |
| `results[].lines[].isTaxable` | boolean |  |
| `results[].lines[].partNumber` | string |  |
| `results[].lines[].quantity` | number |  |
| `results[].lines[].reference` | string |  |
| `results[].lines[].totalAmountExTax` | number |  |
| `results[].lines[].totalAmountIncTax` | number |  |
| `results[].lines[].unitCostExTax` | number |  |
| `results[].sentToAccounts` | boolean |  |
| `results[].supplier.id` | string |  |
| `results[].supplier.name` | string |  |
| `results[].supplierInvoiceId` | string |  |
| `results[].totalAmountExTax` | number |  |
| `results[].totalAmountIncTax` | number |  |
| `results[].trackingNumber` | string |  |
| `results[].type` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Ascora API, this operation is `GET /SupplierInvoices/SupplierInvoices` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supplier-invoices.md) for the provider-specific parameters and requirements.

