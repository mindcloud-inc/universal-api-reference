# List Updates with Range

List updates with optional target, teammate, and time filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/updates`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [List Updates](https://www.range.co/docs/api#rpc-list-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Only fetch updates after this ISO8601 time. |
| `ascending` | query | `boolean` | no | Whether to order oldest first. |
| `before` | query | `string` | no | Only fetch updates before this ISO8601 time. |
| `count` | query | `number` | no | Limit the number of updates returned. |
| `for_user_id` | query | `string` | no | Fetch updates from a user's teammates. |
| `include_child_teams` | query | `boolean` | no | Whether to include descendant-team updates. |
| `include_refs` | query | `boolean` | no | Whether to return snippets, attachments, and users. |
| `target_id` | query | `string` | no | User, team, or organization target ID. |
| `use_client_offset` | query | `boolean` | no | Whether to localize update time to the author's calendar day. |
