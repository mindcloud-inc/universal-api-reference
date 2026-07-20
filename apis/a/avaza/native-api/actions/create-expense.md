# Create Expense with Avaza

Creates a new expense in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Expense`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Expense](https://api.avaza.com/#!/Expense/Expense_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ExpenseDate` | body | `date` | no | The date of the expense entry (Required) |
| `UserIDFK` | body | `number` | no | UserID for a Timesheet/Expense user in Avaza. If not provided, UserEmail field must be provided |
| `UserEmail` | body | `string` | no | The email address of a Timesheet/Expense user in Avaza. If not provided, UserIDFK field must be provided. |
| `ExpenseCategoryIDFK` | body | `number` | no | The expense category to link the Expense to. If not provided, ExpenseCategoryName must be provided |
| `ExpenseCategoryName` | body | `string` | no | Must match an existing expense category name otherwise a new category will be created. If left blank Expense Category ID must be provided. |
| `isChargeable` | body | `boolean` | no | aka Billable. Defaults to false if not provided. If set to true, a CustomerIDFK or CustomerName must be provided. |
| `isReimbursable` | body | `boolean` | no | Defaults to false if not provided. |
| `Quantity` | body | `number` | no | Conditional - available for expenses that are assigned a unit priced based expense category. e.g Mileage |
| `CustomerIDFK` | body | `number` | no | The Avaza Customer ID to associate the Expense with. Either this field or CustomerName can be provided. |
| `CustomerName` | body | `string` | no | The name of an existing customer in Avaza. Must be an exact (case insensitive) match. |
| `ProjectIDFK` | body | `number` | no | The Avaza project ID to associate the Expense with. |
| `ProjectName` | body | `string` | no | Can work for matching an expense to a project, but only if it's an exact match for a single project under the customer. |
| `TaskIDFK` | body | `number` | no | (optional) TaskID of a Task to link the new Expense to. A Customer and Project must be provided also. |
| `CurrencyCode` | body | `string` | no | A 3-letter ISO CurrencyCode for the expense currency. (e.g. USD). If not provided, defaults to the Account base currency. |
| `ExchangeRate` | body | `number` | no | Optional (Only relevant if the expense currency is different to your account currency. If not provided we will look up the market exchange rate for you based on the expense date.) Exchange Rate = Expense Currency Amount / Base Currency Amount (e.g. if Expense currency is in AUD, and Base Currency is in USD, Exchange Rate = AUD $140 / USD $100 = 1.4) |
| `Amount` | body | `number` | no | Expense Amount (Required). Must be &gt;= 0 |
| `TaxIDFK` | body | `number` | no | Avaza Tax ID the expense belongs to. If left blank then Tax Name must be provided. |
| `TaxName` | body | `string` | no | Must exactly match an existing Tax Name that you have configured in Avaza Tax settings. If left blank then Tax ID must be provided. |
| `TransactionTaxConfigCode` | body | `string` | no | Optional - Enter "INC" if the tax amount is included in the expense amount otherwise enter "EX" when the amount exlcudes the tax. Defaults to "Ex". The tax amount on the expense will be autocalculated. |
| `GroupTripName` | body | `string` | no | Links the expense to a Grouping/Trip report. If no matching name found, creates a new Group/Trip Report name. |
| `ExpensePaymentMethodIDFK` | body | `number` | no | (Optional) ID of Expense Payment Method. |
| `Merchant` | body | `string` | no | The name of the merchant. |
| `MerchantTaxNumber` | body | `string` | no | A Tax number identifier for the merchant. |
| `Notes` | body | `string` | no | Expense Notes |
| `VerifyAndSave` | body | `boolean` | no | Pass false if creating a draft expense. True otherwise. |
| `FileAttachmentIDs` | body | `list<number>` | yes | Array of File Attachment IDs to associate with this expense. The files need to have already been uploaded. Currently only accepts a single file. |
