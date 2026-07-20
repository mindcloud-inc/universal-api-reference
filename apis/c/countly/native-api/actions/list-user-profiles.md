# List User Profiles with Countly

Retrieves all user profiles from Countly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o`
- **Base URL:** `https://mindcloud-fe49f15890040.flex.countly.com`
- **Official documentation:** [List User Profiles](https://api.count.ly/reference/omethoduser_details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | query | `string` | yes | Countly app ID to list user profiles for. |
| `iDisplayStart` | query | `number` | no | Offset from which to start displaying users. |
| `iDisplayLength` | query | `number` | no | Number of users to display from the offset. |
| `sSearch` | query | `string` | no | Full-word search on user names or email addresses. |
| `filter` | query | `string` | no | User filter, such as user-all, user-known, or user-anonymous. |
| `query` | query | `string` | no | JSON string encoded MongoDB query for user filtering. |
