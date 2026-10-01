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
| `APInvoices[].APInvoiceDetails[].Amount` | body | `number` | no | — |
| `APInvoices[].APInvoiceDetails[].Distribution.Cost_Center` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Distribution.GL_Account` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Category` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Code` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Item_Description` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Job` | body | `object` | no | — |
| `APInvoices[].APInvoiceDetails[].Job.Cost_Type` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Job.Phase_Code` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Quantity` | body | `number` | no | — |
| `APInvoices[].APInvoiceDetails[].Tax_Code` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Unit_Of_Measure` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order.Component` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order.Equipment` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order.Service_Contract` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order.Unit_Price` | body | `number` | no | — |
| `APInvoices[].Images[].Document_ID` | body | `string` | no | — |
| `APInvoices[].Images[].Image_Description` | body | `string` | no | — |
| `APInvoices[].Images[].Image_File` | body | `string` | no | Base64 |
| `APInvoices[]` | body | `array` | no | — |
| `APInvoices[].APInvoiceDetails[].Distribution` | body | `object` | no | — |
| `APInvoices[].APInvoiceDetails[].Distribution.Company_Code` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Equipment.Equipment_Work_Order` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Job.Job_Number` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order.WO_Number` | body | `string` | no | — |
| `APInvoices[].Images[].Image_Type` | body | `string` | no | — |
| `APInvoices[].Invoice_Number` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Item_Code` | body | `string` | no | — |
| `APInvoices[].Vendor_Code` | body | `string` | no | — |
| `APInvoices[].Approval_Status` | body | `string` | no | — |
| `APInvoices[].Invoice_Type_Code` | body | `string` | no | I — Invoice [default] C — Credit memo |
| `APInvoices[].Routing_Code` | body | `string` | no | — |
| `APInvoices[].GL_Date` | body | `string` | no | Eg: 05/15/2017 |
| `APInvoices[].Invoice_Date` | body | `string` | no | — |
| `APInvoices[].Invoice_Amount` | body | `number` | no | — |
| `APInvoices[].APInvoiceDetails[].Equipment` | body | `object` | no | — |
| `APInvoices[].Sales_Tax_Amount` | body | `number` | no | — |
| `APInvoices[].APInvoiceDetails[].Work_Order` | body | `object` | no | — |
| `APInvoices[].VAT_Code` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[].Remark` | body | `string` | no | — |
| `APInvoices[].Total_VAT_Amount` | body | `string` | no | — |
| `APInvoices[].Contract_Number` | body | `string` | no | — |
| `APInvoices[].Retention_Amount` | body | `number` | no | — |
| `APInvoices[].Batch_Code` | body | `string` | no | — |
| `APInvoices[].Payment_Due_Date` | body | `string` | no | — |
| `APInvoices[].Discount_Due_Date` | body | `string` | no | — |
| `APInvoices[].Discount_Amount` | body | `number` | no | — |
| `APInvoices[].Status` | body | `string` | no | — |
| `APInvoices[].Payment_Status` | body | `string` | no | — |
| `APInvoices[].Bank_Account_Code` | body | `string` | no | — |
| `APInvoices[].Check_Number` | body | `string` | no | — |
| `APInvoices[].Check_Date` | body | `string` | no | — |
| `APInvoices[].Card_Number` | body | `string` | no | — |
| `APInvoices[].AP_GL_Account` | body | `string` | no | — |
| `APInvoices[].Cost_Center` | body | `string` | no | — |
| `APInvoices[].Remarks` | body | `string` | no | — |
| `APInvoices[].APInvoiceDetails[]` | body | `array` | no | — |
| `APInvoices[].Images[]` | body | `array` | no | — |
