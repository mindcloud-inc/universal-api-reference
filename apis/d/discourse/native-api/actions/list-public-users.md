# List Public Users with Discourse

Retrieves public forum users from Discourse.

## Endpoint

- **Method:** `GET`
- **Path:** `/directory_items.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Public Users](https://docs.discourse.org/#tag/Users/operation/listUsersPublic)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asc` | query | `string` | no | Set to true to sort ascending when supported. |
| `order` | query | `string` | yes | Directory sort field such as likes_received or post_count. |
| `page` | query | `string` | no | Directory page number. |
| `period` | query | `string` | yes | Directory period such as daily, weekly, monthly, quarterly, yearly, or all. |
