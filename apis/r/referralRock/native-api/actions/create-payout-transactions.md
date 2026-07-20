# Create Payout Transactions with Referral Rock

Creates payout transactions for pending Referral Rock rewards.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/payouts/transactions`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Create Payout Transactions](https://api.referralrock.com/Help/Api/POST-api-payouts-transactions_overrideIneligible)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `overrideIneligible` | query | `boolean` | no | Allows payouts for rewards with eligibility dates in the future. |
| `memberId` | body | `string` | no | Deprecated member identifier for the payout recipient. |
| `recipientId` | body | `string` | no | The unique ID of the recipient to whom payouts will be issued. |
| `payoutId` | body | `string` | yes | The payout type whose pending amounts should be issued. |
| `note` | body | `string` | no | Message to send to the recipient of the issued payout. |
