# List User Badges with Navigatr

## Endpoint

- **Method:** `GET`
- **Path:** `/user_detail/:user_id/badges`
- **Base URL:** `https://api.navigatr.app/v1`
- **Official documentation:** [List User Badges](https://api.navigatr.app/docs#/User%20Detail/user_detail_read_user_badges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Use 0 for the current user, or a specific user ID such as 19524 when needed. |
| `order_by` | query | `string` | no | Sort order for the user's badges. |
| `keyword` | query | `string` | no | Filter badges by keyword. |
| `status` | query | `string` | no | Filter badges by status. |
