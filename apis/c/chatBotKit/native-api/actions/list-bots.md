# List Bots with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/bot/list`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [List Bots](https://chatbotkit.com/manuals/bots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor for fetching the next page. |
| `order` | query | `list` | no | Order of the paginated items. Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | Number of items to retrieve. |
| `meta` | query | `object` | no | Filter bots by metadata. |
