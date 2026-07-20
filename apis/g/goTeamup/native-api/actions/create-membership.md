# Create Membership with GoTeamup

Creates a new membership in GoTeamup.

## Endpoint

- **Method:** `POST`
- **Path:** `/memberships`
- **Base URL:** `https://goteamup.com/api/v2`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Membership name |
| `type` | body | `string` | yes | Membership type |
| `category` | body | `number` | yes | Membership category |
| `allow_repeat_purchases` | body | `boolean` | yes | Whether repeat purchases are allowed |
| `visible_to_customers` | body | `boolean` | yes | Whether customers can see the membership |
| `purchasable_only_by_provider` | body | `boolean` | yes | Whether only providers can purchase the membership |
| `new_customers_only` | body | `boolean` | yes | Whether only new customers can purchase the membership |
| `one_time_fee` | body | `number` | yes | One-time fee amount |
