# Create Customer Invoice with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddARInvoice`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Customer Invoice](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor-invoices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `GL_Date` | body | `string` | yes |
| `Batch_Code` | body | `string` | yes |
| `Customer_Code` | body | `string` | yes |
| `Job_Number` | body | `string` | no |
| `Invoice_Or_Transaction` | body | `string` | no |
| `Transaction_Type` | body | `list` | yes |
| `Invoice_Date` | body | `date` | yes |
| `Terms_Code` | body | `string` | no |
| `Salesperson_Code` | body | `number` | no |
| `Sales_Tax_Code` | body | `number` | no |
| `Taxable_Flag` | body | `string` | no |
| `Retention_Percent` | body | `string` | no |
| `Print_Job_Address_Flag` | body | `string` | no |
| `Remarks` | body | `string` | no |
| `Customer_PO` | body | `string` | no |
| `AR_GL_Account` | body | `string` | no |
| `Detail_Description` | body | `string` | no |
| `Line_Extension` | body | `string` | no |
| `GL_Account` | body | `string` | no |
| `Sales_Tax_Amount` | body | `number` | no |
| `Retention_Amount` | body | `string` | no |
| `VAT_Code` | body | `string` | no |
| `Total_VAT_Amt` | body | `number` | no |
| `Asset_Cost_Center` | body | `string` | no |
| `Income_Cost_Center` | body | `string` | no |
