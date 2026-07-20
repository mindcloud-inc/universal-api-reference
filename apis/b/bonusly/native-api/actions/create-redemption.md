# Create Redemption with Bonusly

Creates a redemption for a Bonusly user.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:id/redemptions`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [Create Redemption](https://docs.bonus.ly/reference/create-a-redemption)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Redemption amount. |
| `id` | path | `string` | yes | The Bonusly user ID. |
| `reward_id` | body | `string` | yes | Reward identifier. |
