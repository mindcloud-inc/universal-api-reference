# Delete Rewards with Referral Rock

Deletes existing rewards from Referral Rock.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rewards/remove`
- **Base URL:** `https://api.referralrock.com`
- **Official documentation:** [Delete Rewards](https://api.referralrock.com/Help/Api/POST-api-rewards-remove)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `rewardIds[]` | body | `array<string>` | yes |
