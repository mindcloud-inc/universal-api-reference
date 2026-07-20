# Zahara: Get Invoice By ID

Retrieves an invoice by ID from Zahara.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-invoice-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-invoice-by-id?connectionId=$CONNECTION_ID&documentId=22884723" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "22884723"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-invoice-by-id?${params}`, {
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
| `documentId` | number | yes | Invoice document ID. Example: `22884723`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessDivisionId": 1,
      "CreatedBy": 1,
      "CurrencyId": 1,
      "CurrentExportStatus": 1,
      "CurrentExportType": 1,
      "CurrentStepIndex": 1,
      "CustomFieldValues": [
        {
          "DocumentId": 1,
          "Id": 1,
          "TypeId": 1,
          "Value": "string"
        }
      ],
      "DateCreated": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "DocumentId": 1,
      "DueDate": "2026-05-07T12:00:00.000Z",
      "Exported": true,
      "ExportedByWorkflow": true,
      "ExportedDate": "2026-05-07T12:00:00.000Z",
      "InvoiceNumber": "string",
      "InvoiceType": 1,
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "LineItemMatchType": 1,
      "LineItems": [
        {
          "CostCodeId": 1,
          "Description": "string",
          "DiscountPercentage": 1,
          "DivisionId": 1,
          "DocumentId": 1,
          "LineItemId": 1,
          "MatchType": 1,
          "NetValue": 1,
          "NominalCode": "string",
          "NominalCodeId": 1,
          "Price": 1,
          "ProjectId": 1,
          "Quantity": 1,
          "QuantityReceived": 1,
          "TaxCode": "string",
          "TaxCodeId": 1,
          "TaxPercentage": 1,
          "TaxValue": 1
        }
      ],
      "PaymentStatus": 1,
      "PriorityApprovalDocument": true,
      "ProcessStatus": 1,
      "PurchaseOrderNumber": "string",
      "RaisedDate": "2026-05-07T12:00:00.000Z",
      "Status": 1,
      "Supplier": {
        "BusinessUnitId": 1,
        "CountryCode": "string",
        "DefaultCostCodeId": 1,
        "DefaultCurrencyId": 1,
        "DefaultNominalCodeId": 1,
        "DefaultTaxCodeId": 1,
        "IsActive": true,
        "PaymentTermDaysNumber": 1,
        "PaymentTermType": 1,
        "ReferenceNumber": "string",
        "SupplierId": 1,
        "SupplierName": "Ava Chen",
        "TrustedStatus": true
      },
      "SupplierId": 1,
      "TotalGrossValue": 1,
      "TotalNetValue": 1,
      "Type": 1,
      "Void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessDivisionId` | number | Business division ID. |
| `CreatedBy` | number | Creating user ID. |
| `CurrencyId` | number | Currency ID. |
| `CurrentExportStatus` | number | Current export status. |
| `CurrentExportType` | number | Current export type. |
| `CurrentStepIndex` | number | Current workflow step index. |
| `CustomFieldValues[].DocumentId` | number | Custom field document ID. |
| `CustomFieldValues[].Id` | number | Custom field value ID. |
| `CustomFieldValues[].TypeId` | number | Custom field type ID. |
| `CustomFieldValues[].Value` | string | Custom field value. |
| `DateCreated` | date | Creation timestamp. |
| `Description` | string | Invoice description. |
| `DocumentId` | number | Invoice document ID. |
| `DueDate` | date | Invoice due date. |
| `Exported` | boolean | Whether the invoice is exported. |
| `ExportedByWorkflow` | boolean | Whether the invoice was exported by workflow. |
| `ExportedDate` | date | Export timestamp. |
| `InvoiceNumber` | string | Invoice number. |
| `InvoiceType` | number | Invoice type code. |
| `LastUpdated` | date | Last update timestamp. |
| `LineItemMatchType` | number | Line-item match type. |
| `LineItems[].CostCodeId` | number | Invoice cost code ID. |
| `LineItems[].Description` | string | Invoice line item description. |
| `LineItems[].DiscountPercentage` | number | Invoice discount percentage. |
| `LineItems[].DivisionId` | number | Invoice division ID. |
| `LineItems[].DocumentId` | number | Invoice line item document ID. |
| `LineItems[].LineItemId` | number | Invoice line item ID. |
| `LineItems[].MatchType` | number | Invoice line item match type. |
| `LineItems[].NetValue` | number | Invoice line item net value. |
| `LineItems[].NominalCode` | string | Invoice nominal code. |
| `LineItems[].NominalCodeId` | number | Invoice nominal code ID. |
| `LineItems[].Price` | number | Invoice line item price. |
| `LineItems[].ProjectId` | number | Invoice project ID. |
| `LineItems[].Quantity` | number | Invoice quantity. |
| `LineItems[].QuantityReceived` | number | Invoice quantity received. |
| `LineItems[].TaxCode` | string | Invoice tax code. |
| `LineItems[].TaxCodeId` | number | Invoice tax code ID. |
| `LineItems[].TaxPercentage` | number | Invoice tax percentage. |
| `LineItems[].TaxValue` | number | Invoice tax value. |
| `PaymentStatus` | number | Invoice payment status. |
| `PriorityApprovalDocument` | boolean | Whether the invoice is a priority approval document. |
| `ProcessStatus` | number | Process status. |
| `PurchaseOrderNumber` | string | Purchase order number. |
| `RaisedDate` | date | Invoice raised date. |
| `Status` | number | Invoice status. |
| `Supplier.BusinessUnitId` | number | Nested supplier business unit ID. |
| `Supplier.CountryCode` | string | Nested supplier country code. |
| `Supplier.DefaultCostCodeId` | number | Nested supplier default cost code ID. |
| `Supplier.DefaultCurrencyId` | number | Nested supplier default currency ID. |
| `Supplier.DefaultNominalCodeId` | number | Nested supplier default nominal code ID. |
| `Supplier.DefaultTaxCodeId` | number | Nested supplier default tax code ID. |
| `Supplier.IsActive` | boolean | Nested supplier active flag. |
| `Supplier.PaymentTermDaysNumber` | number | Nested supplier payment term day count. |
| `Supplier.PaymentTermType` | number | Nested supplier payment term type. |
| `Supplier.ReferenceNumber` | string | Nested supplier reference number. |
| `Supplier.SupplierId` | number | Nested supplier ID. |
| `Supplier.SupplierName` | string | Nested supplier name. |
| `Supplier.TrustedStatus` | boolean | Nested supplier trusted flag. |
| `SupplierId` | number | Supplier ID. |
| `TotalGrossValue` | number | Total gross value. |
| `TotalNetValue` | number | Total net value. |
| `Type` | number | Invoice type. |
| `Void` | boolean | Whether the invoice is void. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/Invoice/Get/{{documentId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-by-id.md) for the provider-specific parameters and requirements.

