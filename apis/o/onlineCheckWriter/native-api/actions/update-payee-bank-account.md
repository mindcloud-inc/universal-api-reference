# Update Payee Bank Account with OnlineCheckWriter

Updates a specific bank account for a payee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payees/:payeeId/bank-accounts/:payeeBankAccountId`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Update Payee Bank Account](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payeeBankAccountId` | path | `string` | yes | The payee bank account identifier. |
| `payeeId` | path | `string` | yes | The payee identifier. |
