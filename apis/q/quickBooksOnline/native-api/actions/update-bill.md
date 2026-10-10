# Update Bill with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/bill`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Update Bill](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/bill#update-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CurrencyRef.value` | body | `string` | no | — |
| `Id` | body | `string` | yes | ID of the existing bill to update. |
| `Line[].AccountBasedExpenseLineDetail.AccountRef` | body | `object` | yes | — |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.value` | body | `string` | yes | — |
| `Line[].Id` | body | `string` | no | Existing line ID. Include it to keep or modify this line when replacing the bill's lines. |
| `VendorRef.value` | body | `string` | yes | — |
| `Line[].AccountBasedExpenseLineDetail.AccountRef.name` | body | `string` | no | — |
| `Line[].Amount` | body | `number` | yes | — |
| `SyncToken` | body | `string` | yes | Current SyncToken from the bill's latest data, such as a Get Bill or Create Bill result. It changes every time the bill is saved. QuickBooks rejects updates with a stale SyncToken. |
| `Line[].Description` | body | `string` | no | — |
| `VendorRef` | body | `object` | yes | — |
| `Line[]` | body | `array<object>` | no | Sending Line replaces all of the bill's lines; lines not sent are deleted. Include every line you want to keep, and include its existing line Id to keep or modify that line. Omit Line to leave all lines unchanged. |
| `Line[].AccountBasedExpenseLineDetail` | body | `object` | yes | — |
| `DocNumber` | body | `string` | no | Reference number for the transaction (shown as "Ref no." in QuickBooks). Maximum 21 characters. Must be unique unless the company allows duplicates. Maximum length: 21. |
| `TxnDate` | body | `string` | no | Date in yyyy-mm-dd format. |
| `DueDate` | body | `string` | no | Date in yyyy-mm-dd format. |
| `PrivateNote` | body | `string` | no | — |
| `CurrencyRef` | body | `object` | no | — |
