# Create Vendor Invoice with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddAPInvoice`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Vendor Invoice](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AP_GL_Account` | body | `string` | no |
| `Batch_Code` | body | `string` | yes |
| `Contract_Number` | body | `string` | no |
| `Cost_Type` | body | `string` | no |
| `Discount_Amount` | body | `number` | no |
| `Discount_Due_Date` | body | `date` | no |
| `Distribution_GL_Account` | body | `string` | no |
| `Equipment_Category` | body | `string` | no |
| `Equipment_Code` | body | `string` | no |
| `Equipment_Work_Order` | body | `string` | no |
| `Expense_Cost_Center` | body | `string` | no |
| `GL_Date` | body | `string` | yes |
| `Invoice_Amount` | body | `number` | yes |
| `Invoice_Date` | body | `date` | yes |
| `Invoice_Number` | body | `string` | yes |
| `Invoice_Type_Code` | body | `list` | yes |
| `Item_Code` | body | `string` | no |
| `Job_Number` | body | `string` | no |
| `Liability_Cost_Center` | body | `string` | no |
| `Payment_Due_Date` | body | `date` | no |
| `Phase_Code` | body | `string` | no |
| `PO_Number` | body | `string` | no |
| `Quantity` | body | `number` | no |
| `Remarks` | body | `string` | no |
| `Retention_Amount` | body | `number` | no |
| `Sales_Tax_Amount` | body | `number` | no |
| `Status` | body | `list` | no |
| `Tax_Code` | body | `string` | no |
| `Total_VAT_Amt` | body | `number` | no |
| `VAT_Code` | body | `string` | no |
| `Vendor_Code` | body | `string` | yes |
| `WO_Component` | body | `string` | no |
| `WO_Equipment` | body | `string` | no |
| `WO_Number` | body | `string` | no |
| `WO_SC_Contract` | body | `string` | no |
| `WO_Unit_Price` | body | `number` | no |
