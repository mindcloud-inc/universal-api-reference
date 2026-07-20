# Search Messages with Pachca (Admin)

Finds messages in the Pachca Admin API by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/messages`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Search Messages](https://dev.pachca.com/search/list-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter by active chats. |
| `chat_ids[]` | query | `array<number>` | no | Filter by chat ids. |
| `created_from` | query | `date` | no | Filter messages created on or after this timestamp. |
| `created_to` | query | `date` | no | Filter messages created on or before this timestamp. |
| `cursor` | query | `string` | no | Pagination cursor from meta.paginate.next_page. |
| `limit` | query | `number` | no | Number of results to return. |
| `order` | query | `string` | no | Sort direction. |
| `query` | query | `string` | no | Full-text search string. |
| `user_ids[]` | query | `array<number>` | no | Filter by author user ids. |
