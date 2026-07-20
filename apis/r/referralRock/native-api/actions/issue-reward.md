# Issue Reward with Referral Rock

Issues a specific reward in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rewards/issue`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Issue Reward](https://api.referralrock.com/Help/Api/POST-api-rewards-issue_overrideIneligible)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `overrideIneligible` | query | `boolean` | no | Allows issuing rewards with eligibility dates in the future. |
| `rewardId` | body | `string` | yes | The unique ID of the reward to issue. |
| `recipientInfo` | body | `string` | no | Deprecated extra recipient info; for PayPal this can include the recipient email address. |
| `note` | body | `string` | no | Message to send to the reward recipient. |
