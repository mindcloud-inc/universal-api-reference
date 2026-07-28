# Upload a new memo for a transaction with Ramp

## Endpoint

- **Method:** `POST`
- **Path:** `memos/:transactionId`
- **Base URL:** `https://api.ramp.com/developer/v1/`
- **Official documentation:** [Upload a new memo for a transaction](https://docs.ramp.com/developer-api/v1/api/transactions#get-developer-v1-transactions-transaction-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `transactionId` | path | `string` | no |
| `memo` | body | `string` | yes |
