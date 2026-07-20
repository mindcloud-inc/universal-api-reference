# Create Payee Bank Account with OnlineCheckWriter

Creates a bank account for a specific payee.

## Endpoint

- **Method:** `POST`
- **Path:** `/payees/:payeeId/bank-accounts`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Create Payee Bank Account](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payeeId` | path | `string` | yes | The payee identifier. |
