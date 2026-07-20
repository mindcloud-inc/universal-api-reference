# Update Invoice with Avaza

Updates an existing invoice in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Invoice`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Invoice](https://api.avaza.com/#!/Invoice/Invoice_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FieldsToUpdate` | body | `list<string>` | yes | Required: The collection of Field Names you wish to update. Possible Values: CustomerPONumber, DateIssued, PaymentTerms, DueDate, Subject, Notes, TransactionTaxConfigCode, ExchangeRate, InvoiceTemplateIDFK, InvoiceNumber, LineItems |
| `TransactionID` | body | `number` | yes | The ID of the Invoice to update |
| `CustomerPONumber` | body | `string` | no | Plain UTF8 text. 100 characters max |
| `DateIssued` | body | `date` | no | The Date the Invoice is issued. Date should be specified as local date. |
| `PaymentTerms` | body | `number` | no | — |
| `DueDate` | body | `date` | no | If the Due Date is specified then Payment Terms will be set to -1 (Custom). Otherwise DueDate will be auto calculated based on the provided IssueDate and Payment Term. Due Date must be greater than or equal to Issue Date. |
| `Subject` | body | `string` | no | Invoice Subject in plain UTF8 text. (no HTML). 255 characters max |
| `Notes` | body | `string` | no | Invoice Notes in plain UTF8 text. (no HTML). Max 2000 characters |
| `TransactionTaxConfigCode` | body | `string` | no | Possible values are (EX --- Tax Exclusive, INC --- Tax Inclusive). If left set to null/emptystring it will use the account default. |
| `ExchangeRate` | body | `number` | no | Exchange rate is only valid for invoices in currency other than default account currency. If not specified it will get the market rate based on the Date Issued. |
| `InvoiceTemplateIDFK` | body | `number` | no | And id for an invoice template in the account. If set to Null the account default invoice template will be used. |
| `InvoiceNumber` | body | `string` | no | Pass a string or integer. If an integer is passed then the largest integer will be use as the seed to auto generate the next invoice number in the sequence. |
| `LineItems` | body | `list<object>` | yes | — |
| `TransactionLineItemID` | body | `number` | no | Optional ID of exisiting TransactionLineItem that should be retained and updated |
| `InventoryItemIDFK` | body | `number` | yes | The ID of the InventoryItem this line item is linked to |
| `Description` | body | `string` | no | Plain UTF8 text. (no HTML) |
| `Quantity` | body | `number` | yes | The quantity for the line item |
| `UnitPrice` | body | `number` | yes | The unit price for the lineitem. |
| `TaxIDFK` | body | `number` | no | Must match an existing Tax ID. |
| `Discount` | body | `number` | no | Enter 10.5 to give a 10.5% discount |
| `ProjectIDFK` | body | `number` | no | Optional. Project ID of an Avaza Project that belongs to this customer, so line item is attributed to that Project for reporting. |
