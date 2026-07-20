# List Users with Sendbird

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api-{applicationId}.sendbird.com/v3`
- **Official documentation:** [List Users](https://docs.sendbird.com/docs/chat/platform-api/v3/user/listing-users/list-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of users to return per page. Acceptable values are 1 to 100. |
| `token` | query | `string` | no | Page token indicating the starting index of results to retrieve. |
| `active_mode` | query | `string` | no | Activation status filter: activated, deactivated, or all. |
| `show_bot` | query | `boolean` | no | Include bots in the result set. |
| `user_ids` | query | `string` | no | Comma-separated urlencoded user IDs to include. |
| `nickname` | query | `string` | no | Exact nickname filter. |
| `nickname_startswith` | query | `string` | no | Prefix filter for nicknames. |
| `metadatakey` | query | `string` | no | Metadata key to filter on when paired with metadata values. |
| `metadatavalues_in` | query | `string` | no | Comma-separated metadata values used with Metadata Key. |
