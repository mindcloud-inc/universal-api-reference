# Redeem Reward with Reward Sciences

## Endpoint

- **Method:** `POST`
- **Path:** `/rewards/:rewardId/redemptions`
- **Base URL:** `https://api.rewardsciences.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rewardId` | path | `number` | yes | The Reward Sciences reward ID. |
| `user_id` | body | `number` | yes | The user redeeming the reward. |
