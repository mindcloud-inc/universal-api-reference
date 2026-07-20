# Fulfill Custom Reward Redemptions with Bonusly

Fulfills custom reward redemptions in Bonusly.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom_rewards_redemptions/fulfill`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Fulfill Custom Reward Redemptions](https://docs.bonus.ly/reference/fulfill-custom-reward-redemptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_list` | body | `string` | no | Custom reward redemption IDs to fulfill. |
