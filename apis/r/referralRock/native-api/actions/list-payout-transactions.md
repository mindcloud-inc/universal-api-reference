# List Payout Transactions with Referral Rock

Retrieves payout transactions from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/payouts/transactions`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [List Payout Transactions](https://api.referralrock.com/Help/Api/GET-api-payouts-transactions_recipientId_transactionId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientId` | query | `string` | no | The unique ID of the recipient of the payout transaction. |
| `transactionId` | query | `string` | no | The unique ID of the payout transaction. |
