# Redeem Rewards By Unique Card Data Field with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/uniquecard/campaignid/:campaignId/:uniqueIdType/:uniqueIdValue/redeemReward/:rewardType/:rewardsToRedeem`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Redeem Rewards By Unique Card Data Field](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_redeemRewardByUniqueCardField)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `string` | yes |
| `uniqueIdType` | path | `string` | yes |
| `uniqueIdValue` | path | `string` | yes |
| `rewardType` | path | `number` | yes |
| `rewardsToRedeem` | path | `number` | yes |
| `scanLatitude` | body | `number` | no |
| `scanLongitude` | body | `number` | no |
