# Zahara: Get Purchase Order By ID

Retrieves a purchase order by ID from Zahara.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-purchase-order-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-purchase-order-by-id?connectionId=$CONNECTION_ID&documentId=34070" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "34070"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/get-purchase-order-by-id?${params}`, {
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
| `documentId` | number | yes | Purchase order document ID. Example: `34070`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessDivisionId": 1,
      "CurrencyId": 1,
      "CurrentExportStatus": 1,
      "CurrentExportType": 1,
      "CurrentStepIndex": 1,
      "DateCreated": "2026-05-07T12:00:00.000Z",
      "DocumentId": 1,
      "Exported": true,
      "ExportedByWorkflow": true,
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
          "RequiredDate": "2026-05-07T12:00:00.000Z",
          "TaxCode": "string",
          "TaxCodeId": 1,
          "TaxPercentage": 1,
          "TaxValue": 1
        }
      ],
      "PriorityApprovalDocument": true,
      "ProcessStatus": 1,
      "PurchaseOrderNumber": "string",
      "RequiredDate": "2026-05-07T12:00:00.000Z",
      "RequisitorId": 1,
      "Status": 1,
      "Supplier": {
        "CountryCode": "string",
        "CountryCodeId": 1,
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
| `CurrencyId` | number | Currency ID. |
| `CurrentExportStatus` | number | Current export status. |
| `CurrentExportType` | number | Current export type. |
| `CurrentStepIndex` | number | Current workflow step index. |
| `DateCreated` | date | Creation timestamp. |
| `DocumentId` | number | Purchase order document ID. |
| `Exported` | boolean | Whether the purchase order is exported. |
| `ExportedByWorkflow` | boolean | Whether the purchase order was exported by workflow. |
| `LastUpdated` | date | Last update timestamp. |
| `LineItemMatchType` | number | Line-item match type. |
| `LineItems[].CostCodeId` | number | Purchase order cost code ID. |
| `LineItems[].Description` | string | Purchase order line item description. |
| `LineItems[].DiscountPercentage` | number | Purchase order discount percentage. |
| `LineItems[].DivisionId` | number | Purchase order division ID. |
| `LineItems[].DocumentId` | number | Purchase order line item document ID. |
| `LineItems[].LineItemId` | number | Purchase order line item ID. |
| `LineItems[].MatchType` | number | Purchase order line item match type. |
| `LineItems[].NetValue` | number | Purchase order line item net value. |
| `LineItems[].NominalCode` | string | Purchase order nominal code. |
| `LineItems[].NominalCodeId` | number | Purchase order nominal code ID. |
| `LineItems[].Price` | number | Purchase order line item price. |
| `LineItems[].ProjectId` | number | Purchase order project ID. |
| `LineItems[].Quantity` | number | Purchase order quantity. |
| `LineItems[].QuantityReceived` | number | Purchase order quantity received. |
| `LineItems[].RequiredDate` | date | Purchase order line item required date. |
| `LineItems[].TaxCode` | string | Purchase order tax code. |
| `LineItems[].TaxCodeId` | number | Purchase order tax code ID. |
| `LineItems[].TaxPercentage` | number | Purchase order tax percentage. |
| `LineItems[].TaxValue` | number | Purchase order tax value. |
| `PriorityApprovalDocument` | boolean | Whether the purchase order is a priority approval document. |
| `ProcessStatus` | number | Process status. |
| `PurchaseOrderNumber` | string | Purchase order number. |
| `RequiredDate` | date | Required date. |
| `RequisitorId` | number | Requisitor user ID. |
| `Status` | number | Purchase order status. |
| `Supplier.CountryCode` | string | Nested supplier country code. |
| `Supplier.CountryCodeId` | number | Nested supplier country code ID. |
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
| `Type` | number | Purchase order type. |
| `Void` | boolean | Whether the purchase order is void. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/PurchaseOrder/Get/{{documentId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order-by-id.md) for the provider-specific parameters and requirements.

