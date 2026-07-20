# Create Bill with Avaza

Creates a new bill in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Bill`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Bill](https://api.avaza.com/#!/Bill/Bill_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionPrefix` | body | `string` | no | A prefix for the Invoice number. e.g. 'INV'. If left blank it will be set to the account default. Max length 20 characters. |
| `BillNumber` | body | `string` | no | Pass any string. If left blank it will use the next number in the auto incrementing sequence. If an integer is passed then the largest integer will be use as the seed to auto generate the next invoice number in the sequence. |
| `CompanyIDFK` | body | `number` | no | If left blank then you must specify Company Name. |
| `CompanyName` | body | `string` | no | If left blank then you must specify Company ID. Specified Name will be used to match existing customer record. If not matched then it will be used to create a new customer. First Name, Last Name and Email will only be used if it is a new company. If the Company name appears multiple times we will check the email address to find a matching company. If email address doesn't identify a matching company then the invoice creation will be rejected. |
| `Firstname` | body | `string` | no | Specified value will be used to create a new customer contact only if a new customer is being created. |
| `Lastname` | body | `string` | no | Specified value will be used to create a new customer contact only if a new customer is being created. |
| `Email` | body | `string` | no | Specified value will be used to create a new customer contact only if a new customer is being created. |
| `CurrencyCode` | body | `string` | no | Expects ISO Standard 3 character currency code. If left blank the currency will default to account's currency in general setting. For existing companies this field will be ignored and the invoice will use the currency of the customer. For new customers if the currency is not specified then account currency will be used otherwise the specified currency will be used. |
| `ExchangeRate` | body | `number` | no | Exchange rate is only valid for invoices in currency other than default account currency. If not specified it will get the market rate based on the Date Issued. |
| `BillTemplateIDFK` | body | `number` | no | If left blank the account default invoice template will be used. |
| `Subject` | body | `string` | no | Plain UTF8 text. (no HTML). 255 characters max |
| `SupplierPONumber` | body | `string` | no | Plain UTF8 text. 100 characters max |
| `DateIssued` | body | `date` | no | If not specified it will use today's date. The date should be specified as local date. |
| `PaymentTerms` | body | `number` | no | "If left blank we will set it to customer default. If specified then it must match one of your existing pre configured payment term periods. Your account starts with: (-1 --- Custom, 0 --- Upon Receipt, 7 --- 7 Days, 15 --- 15 Days, 30 --- 30 Days, 45 --- 45 Days, 60 --- 60 Days) |
| `DueDate` | body | `date` | no | It will be auto calculated based on the payment term and issue date. Due Date must be greater than or equal to Issue Date. If the Due Date is specified then Payment Terms will be set to -1 (Custom) |
| `TransactionTaxConfigCode` | body | `string` | no | Possible values are (EX --- Tax Exclusive, INC --- Tax Inclusive). If left empty it will use the account default. |
| `Notes` | body | `string` | no | Plain UTF8 text. (no HTML). Max 2000 characters |
| `LineItems` | body | `list<object>` | yes | — |
| `InventoryItemIDFK` | body | `number` | no | If not specified then Inventory Item Name must be specified. |
| `InventoryItemName` | body | `string` | no | If not specified then Inventory item ID must be specified. If specified and not matched to any existing inventory items then a new inventory item will be created. Max 200 characters. |
| `Description` | body | `string` | no | Plain UTF8 text. (no HTML) |
| `Quantity` | body | `number` | yes | The quantity for the line item |
| `UnitPrice` | body | `number` | yes | The unit price for the lineitem. |
| `TaxIDFK` | body | `number` | no | If specified then it must match an existing Tax ID. If not specified then Tax Name and Tax Percent must be specified. |
| `TaxName` | body | `string` | no | Must be specified if the Tax ID is blank. If the Tax Name is specified it will be matched to an existing Tax Name or else a new Tax will be created. |
| `TaxPercent` | body | `number` | no | The Tax Percent will only be used if a new tax is being created. |
| `Discount` | body | `number` | no | Enter 10.5 to give a 10.5% discount |
| `ProjectIDFK` | body | `number` | no | Optional. Project ID of an Avaza Project that belongs to this customer, so line item is attributed to that Project for reporting. |
