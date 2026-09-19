# Create AR Customer Invoice Multi-Line with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `customer/invoice`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create AR Customer Invoice Multi-Line](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/multi-line-customer-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arInvoices[]` | body | `array` | no | — |
| `arInvoices[].multiLineArInvoice` | body | `object` | no | — |
| `arInvoices[].multiLineArInvoice.Company_Code` | body | `string` | yes | Maximum length: 3. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail` | body | `object` | no | — |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Quantity` | body | `number` | no | — |
| `arInvoices[].multiLineArInvoice.GL_Date` | body | `string` | yes | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Detail_Description` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Batch_Code` | body | `string` | yes | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Unit_Of_Measure` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Customer_Code` | body | `string` | yes | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Line_Extension` | body | `number` | yes | — |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.GL_Account` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Job Number` | body | `string` | no | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.Invoice_Or_Transaction` | body | `string` | yes | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Taxable_Flag` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Income_Cost_Center` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Transaction_Type` | body | `string` | yes | Maximum length: 1. |
| `arInvoices[].multiLineArInvoice.Invoice Date` | body | `string` | yes | Maximum length: 10. |
| `arInvoices[].multiLineArInvoice.invoiceDetails[].invoiceDetail.Message` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Terms_Code` | body | `string` | no | Maximum length: 1. |
| `arInvoices[].multiLineArInvoice.Salesperson_Code` | body | `string` | no | Maximum length: 3. |
| `arInvoices[].multiLineArInvoice.Sales_Tax_Code` | body | `string` | no | Maximum length: 15. |
| `arInvoices[].multiLineArInvoice.Sale_Tax_Amount` | body | `number` | no | Maximum length: 13. |
| `arInvoices[].multiLineArInvoice.Retention_Percent` | body | `number` | no | Maximum length: 6. |
| `arInvoices[].multiLineArInvoice.Print_Job_Address_Flag` | body | `string` | no | Maximum length: 1. |
| `arInvoices[].multiLineArInvoice.Remarks` | body | `string` | no | Maximum length: 65. |
| `arInvoices[].multiLineArInvoice.Customer_PO` | body | `string` | no | Maximum length: 25. |
| `arInvoices[].multiLineArInvoice.Retention_Amount` | body | `number` | no | — |
| `arInvoices[].multiLineArInvoice.VAT_Code` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.Total_Vat_Amount` | body | `number` | no | — |
| `arInvoices[].multiLineArInvoice.Asset_Cost_Center` | body | `string` | no | — |
| `arInvoices[].multiLineArInvoice.invoiceDetails[]` | body | `array` | no | — |
