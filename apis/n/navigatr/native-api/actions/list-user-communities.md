# List User Communities with Navigatr

## Endpoint

- **Method:** `GET`
- **Path:** `/user_detail/:user_id/communities`
- **Base URL:** `https://api.navigatr.app/v1`
- **Official documentation:** [List User Communities](https://api.navigatr.app/docs#/User%20Detail/user_detail_read_user_communities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Use 0 for the current user, or a specific user ID such as 19524 when needed. |
