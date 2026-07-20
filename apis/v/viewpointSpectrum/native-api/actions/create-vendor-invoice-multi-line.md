# Create Vendor Invoice Multi-Line with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `vendor/invoice`
- **Base URL:** `{url}:8482/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `APInvoiceDetails[].Amount` | body | `number` | no | — |
| `APInvoiceDetails[].Distribution.Cost_Center` | body | `string` | no | — |
| `APInvoiceDetails[].Distribution.GL_Account` | body | `string` | no | — |
| `APInvoiceDetails[].Equipment.Equipment_Category` | body | `string` | no | — |
| `APInvoiceDetails[].Equipment.Equipment_Code` | body | `string` | no | — |
| `APInvoiceDetails[].Item_Description` | body | `string` | no | — |
| `APInvoiceDetails[].Job` | body | `object` | no | — |
| `APInvoiceDetails[].Job.Cost_Type` | body | `string` | no | — |
| `APInvoiceDetails[].Job.Phase_Code` | body | `string` | no | — |
| `APInvoiceDetails[].Quantity` | body | `number` | no | — |
| `APInvoiceDetails[].Tax_Code` | body | `string` | no | — |
| `APInvoiceDetails[].Unit_Of_Measure` | body | `string` | no | — |
| `APInvoiceDetails[].Work_Order.Component` | body | `string` | no | — |
| `APInvoiceDetails[].Work_Order.Equipment` | body | `string` | no | — |
| `APInvoiceDetails[].Work_Order.Service_Contract` | body | `string` | no | — |
| `APInvoiceDetails[].Work_Order.Unit_Price` | body | `number` | no | — |
| `Images[].Document_ID` | body | `string` | no | — |
| `Images[].Image_Description` | body | `string` | no | — |
| `Images[].Image_File` | body | `string` | no | Base64 |
| `APInvoiceDetails[].Distribution` | body | `object` | no | — |
| `APInvoiceDetails[].Distribution.Company_Code` | body | `string` | no | — |
| `APInvoiceDetails[].Equipment.Equipment_Work_Order` | body | `string` | no | — |
| `APInvoiceDetails[].Job.Job_Number` | body | `string` | no | — |
| `APInvoiceDetails[].Work_Order.WO_Number` | body | `string` | no | — |
| `Images[].Image_Type` | body | `string` | no | — |
| `Invoice_Number` | body | `string` | no | — |
| `APInvoiceDetails[].Item_Code` | body | `string` | no | — |
| `Vendor_Code` | body | `string` | no | — |
| `Approval_Status` | body | `string` | no | — |
| `Invoice_Type_Code` | body | `string` | no | I — Invoice [default] C — Credit memo |
| `Routing_Code` | body | `string` | no | — |
| `GL_Date` | body | `string` | no | Eg: 05/15/2017 |
| `Invoice_Date` | body | `string` | no | — |
| `Invoice_Amount` | body | `number` | no | — |
| `APInvoiceDetails[].Equipment` | body | `object` | no | — |
| `Sales_Tax_Amount` | body | `number` | no | — |
| `APInvoiceDetails[].Work_Order` | body | `object` | no | — |
| `VAT_Code` | body | `string` | no | — |
| `APInvoiceDetails[].Remark` | body | `string` | no | — |
| `Total_VAT_Amount` | body | `string` | no | — |
| `Contract_Number` | body | `string` | no | — |
| `Retention_Amount` | body | `number` | no | — |
| `Batch_Code` | body | `string` | no | — |
| `Payment_Due_Date` | body | `string` | no | — |
| `Discount_Due_Date` | body | `string` | no | — |
| `Discount_Amount` | body | `number` | no | — |
| `Status` | body | `string` | no | — |
| `Payment_Status` | body | `string` | no | — |
| `Bank_Account_Code` | body | `string` | no | — |
| `Check_Number` | body | `string` | no | — |
| `Check_Date` | body | `string` | no | — |
| `Card_Number` | body | `string` | no | — |
| `AP_GL_Account` | body | `string` | no | — |
| `Cost_Center` | body | `string` | no | — |
| `Remarks` | body | `string` | no | — |
| `APInvoiceDetails[]` | body | `array` | no | — |
| `Images[]` | body | `array` | no | — |
