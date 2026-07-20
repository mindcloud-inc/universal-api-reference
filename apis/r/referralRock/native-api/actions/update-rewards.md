# Update Rewards with Referral Rock

Updates existing rewards in Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rewards/update`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Update Rewards](https://api.referralrock.com/Help/Api/POST-api-rewards-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no |
| `items[].description` | body | `string` | no |
| `items[].rewardId` | body | `string` | yes |
| `items[].amount` | body | `number` | no |
| `items[].payoutId` | body | `string` | yes |
| `items[].eligibilityDate` | body | `date` | no |
