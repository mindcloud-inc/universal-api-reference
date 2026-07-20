# Search Bank Transactions with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/bank/search`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Bank Transactions](https://api.quickfile.co.uk/d/v1_2/Bank_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AmountFrom` | body | `number` | no | Lower bound for transaction amount |
| `AmountTo` | body | `number` | no | Upper bound for transaction amount |
| `FromDate` | body | `date` | no | Lower bound for transaction date |
| `NominalCode` | body | `number` | yes | Nominal code of the bank account to query |
| `Notes` | body | `string` | no | Whole or partial transaction notes |
| `Offset` | body | `number` | yes | Page offset for bank transaction results |
| `OrderDirection` | body | `string` | yes | Direction used to order the transaction results |
| `OrderResultsBy` | body | `string` | yes | Column used to order the transaction results |
| `Reference` | body | `string` | no | Whole or partial transaction reference |
| `ReturnCount` | body | `number` | yes | Maximum number of bank transactions to return |
| `ToDate` | body | `date` | no | Upper bound for transaction date |
| `TransactionType` | body | `string` | no | credits, debits, or omit for both |
