# List Payee Bank Accounts with OnlineCheckWriter

Lists bank accounts for a specific payee.

## Endpoint

- **Method:** `GET`
- **Path:** `/payees/:payeeId/bank-accounts/`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [List Payee Bank Accounts](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payeeId` | path | `string` | yes | The payee identifier. |
