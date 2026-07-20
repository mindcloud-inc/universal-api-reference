# Search Chats with Pachca (Admin)

Finds chats in the Pachca Admin API by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/chats`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Search Chats](https://dev.pachca.com/search/list-chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter by active chats. |
| `chat_subtype` | query | `string` | no | Filter by chat subtype. |
| `created_from` | query | `date` | no | Filter chats created on or after this timestamp. |
| `created_to` | query | `date` | no | Filter chats created on or before this timestamp. |
| `cursor` | query | `string` | no | Pagination cursor from meta.paginate.next_page. |
| `limit` | query | `number` | no | Number of results to return. |
| `order` | query | `string` | no | Sort direction. |
| `personal` | query | `boolean` | no | Filter personal chats only. |
| `query` | query | `string` | no | Full-text search string. |
