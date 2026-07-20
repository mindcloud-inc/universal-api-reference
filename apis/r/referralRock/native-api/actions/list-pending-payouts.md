# List Pending Payouts with Referral Rock

Retrieves pending payouts from Referral Rock.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/payouts/pending`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [List Pending Payouts](https://api.referralrock.com/Help/Api/GET-api-payouts-pending_memberId_recipientId_includeIneligible)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeIneligible` | query | `boolean` | no | Include payouts for rewards with future eligibility dates. |
| `memberId` | query | `string` | no | The unique ID of the member to whom the amount is owed. Deprecated. |
| `recipientId` | query | `string` | no | The unique ID of the recipient to whom the amount is owed. |
