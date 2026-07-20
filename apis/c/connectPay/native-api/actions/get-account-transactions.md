# Get Account Transactions with ConnectPay

Retrieves bank account transactions from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/accounts/:accountId/transactions`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Account Transactions](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getAccountTransactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | ID of the account. |
| `dateFrom` | query | `string` | no | Start of the transaction period in YYYY-MM-DD format. |
| `dateTo` | query | `string` | no | End of the transaction period in YYYY-MM-DD format. |
| `sortOrder` | query | `string` | no | Sorting order of transactions, asc or desc. |
