# List Conversations with EZ Texting

Retrieves conversations from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Conversations](https://developers.eztexting.com/reference/list_3-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[archived][eq]` | query | `string` | no | Filter conversations by archive state |
| `filters[from][eq]` | query | `string` | no | Filter conversations by sender number |
| `filters[optType][eq]` | query | `string` | no | Filter conversations by opt type |
| `filters[query][eq]` | query | `string` | no | Filter conversations by text query |
| `filters[unread][eq]` | query | `string` | no | Filter conversations by unread state |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
