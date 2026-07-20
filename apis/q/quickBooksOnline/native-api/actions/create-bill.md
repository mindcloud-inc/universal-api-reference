# Create Bill with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/billpayment`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Create Bill](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/bill#create-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CheckPayment.BankAccountRef` | body | `object` | no | — |
| `CheckPayment.BankAccountRef.name` | body | `string` | no | — |
| `CurrencyRef.value` | body | `string` | no | — |
| `Line[].Amount` | body | `number` | no | — |
| `Line[].LinkedTxn[].TxnId` | body | `string` | no | — |
| `VendorRef` | body | `object` | no | — |
| `VendorRef.value` | body | `string` | yes | Vendor Id for the bill. |
| `CheckPayment.BankAccountRef.value` | body | `string` | no | — |
| `Line[].LinkedTxn[]` | body | `array` | no | — |
| `Line[].LinkedTxn[].TxnType` | body | `string` | no | — |
| `TotalAmt` | body | `number` | no | — |
| `payType` | body | `string` | no | — |
| `PrivateNote` | body | `string` | no | — |
| `TxnDate` | body | `string` | no | — |
| `CurrencyRef` | body | `object` | no | — |
| `Line[]` | body | `array` | no | — |
| `CheckPayment` | body | `object` | no | — |
