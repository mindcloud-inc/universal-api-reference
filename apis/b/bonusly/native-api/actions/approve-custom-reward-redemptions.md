# Approve Custom Reward Redemptions with Bonusly

Approves custom reward redemptions in Bonusly.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom_rewards_redemptions/approve`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Approve Custom Reward Redemptions](https://docs.bonus.ly/reference/approve-custom-reward-redemptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_list` | body | `string` | yes | Custom reward redemption IDs to approve. |
| `state` | body | `string` | no | Optional approval state value. |
