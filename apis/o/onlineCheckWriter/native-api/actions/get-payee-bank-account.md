# Get Payee Bank Account with OnlineCheckWriter

Retrieves a specific bank account for a payee.

## Endpoint

- **Method:** `GET`
- **Path:** `/payees/:payeeId/bank-accounts/:payeeBankAccountId`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Get Payee Bank Account](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payeeBankAccountId` | path | `string` | yes | The payee bank account identifier. |
| `payeeId` | path | `string` | yes | The payee identifier. |
