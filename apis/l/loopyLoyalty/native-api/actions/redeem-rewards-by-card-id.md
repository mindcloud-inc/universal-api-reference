# Redeem Rewards By Card ID with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/card/cid/:cid/redeemReward/:rewardType/:rewardsToRedeem`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Redeem Rewards By Card ID](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_redeemReward)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cid` | path | `string` | yes |
| `rewardType` | path | `number` | yes |
| `rewardsToRedeem` | path | `number` | yes |
| `scanLatitude` | body | `number` | no |
| `scanLongitude` | body | `number` | no |
