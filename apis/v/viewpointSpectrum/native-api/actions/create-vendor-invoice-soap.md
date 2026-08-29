# Create Vendor Invoice (SOAP) with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddAPInvoice`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Vendor Invoice (SOAP)](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchCode` | body | `string` | no | — |
| `vendorCode` | body | `string` | yes | Maximum length: 20. |
| `GL_Date` | body | `string` | no | — |
| `contractNumber` | body | `string` | no | Maximum length: 20. |
| `invoiceNumber` | body | `string` | no | Maximum length: 30. |
| `invoiceTypeCode` | body | `string` | no | Maximum length: 30. |
| `invoiceDate` | body | `string` | no | — |
| `invoiceAmount` | body | `string` | no | Maximum length: 25. |
| `salesTaxAmount` | body | `string` | no | Maximum length: 20. |
| `retentionAmount` | body | `string` | no | Maximum length: 20. |
| `paymentDueDate` | body | `string` | no | Maximum length: 20. |
| `status` | body | `string` | no | — |
| `discountDueDate` | body | `string` | no | Maximum length: 20. |
| `discountAmount` | body | `string` | no | Maximum length: 20. |
| `remarks` | body | `string` | no | Maximum length: 20. |
| `apGlAccount` | body | `string` | no | Maximum length: 20. |
| `distributionGlAccount` | body | `string` | no | Maximum length: 20. |
| `jobNumber` | body | `string` | no | Maximum length: 20. |
| `phaseCode` | body | `string` | no | — |
| `costType` | body | `string` | no | — |
| `equipmentCode` | body | `string` | no | — |
| `equipmentCategory` | body | `string` | no | — |
| `equipmentWorkOrder` | body | `string` | no | — |
| `woNumber` | body | `string` | no | — |
| `itemCode` | body | `string` | no | Maximum length: 15. |
| `quantity` | body | `string` | no | Maximum length: 15. |
| `woEquipment` | body | `string` | no | — |
| `woComponent` | body | `string` | no | — |
| `woServiceContract` | body | `string` | no | — |
| `woUnitPrice` | body | `string` | no | — |
| `taxCode` | body | `string` | no | Maximum length: 50. |
| `vatCode` | body | `string` | no | — |
| `totalVatAmount` | body | `string` | no | — |
| `liabilityCostCenter` | body | `string` | no | — |
| `expenseCostCenter` | body | `string` | no | — |
