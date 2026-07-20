# Update Membership with GoTeamup

Updates an existing membership in GoTeamup.

## Endpoint

- **Method:** `PUT`
- **Path:** `/memberships/:id`
- **Base URL:** `https://goteamup.com/api/v2`
- **Official documentation:** [Update Membership](https://docs.goteamup.com/api-reference/endpoints/memberships)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The TeamUp membership ID |
| `name` | body | `string` | no | Updated membership name |
| `category` | body | `number` | yes | Membership category ID. |
| `allow_repeat_purchases` | body | `boolean` | yes | Allow repeat purchases. |
| `visible_to_customers` | body | `boolean` | yes | Visible to customers. |
| `purchasable_only_by_provider` | body | `boolean` | yes | Whether only providers can purchase. |
| `new_customers_only` | body | `boolean` | yes | Only available to new customers. |
| `one_time_fee` | body | `number` | yes | One-time membership fee. |
