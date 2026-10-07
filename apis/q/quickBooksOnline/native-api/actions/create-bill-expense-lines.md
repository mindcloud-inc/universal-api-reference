# Create Bill (Expense Lines) with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/bill`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Bill (Expense Lines)](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/bill#create-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CurrencyRef.value` | body | `string` | no | — |
| `Line[].AccountBasedExpenseLineDetail.AccountRef` | body | `object` | yes | — |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.value` | body | `string` | yes | — |
| `Line[].Amount` | body | `number` | yes | — |
| `VendorRef` | body | `object` | yes | — |
| `VendorRef.value` | body | `string` | yes | — |
| `Line[]` | body | `array<object>` | yes | — |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.name` | body | `string` | no | — |
| `DocNumber` | body | `string` | no | Reference number for the transaction (shown as "Ref no." in QuickBooks). Maximum 21 characters. Must be unique unless the company allows duplicates. Maximum length: 21. |
| `Line[].Description` | body | `string` | no | — |
| `Line[].AccountBasedExpenseLineDetail` | body | `object` | yes | — |
| `TxnDate` | body | `string` | no | Date in yyyy-mm-dd format. |
| `DueDate` | body | `string` | no | Date in yyyy-mm-dd format. |
| `PrivateNote` | body | `string` | no | — |
| `CurrencyRef` | body | `object` | no | — |
