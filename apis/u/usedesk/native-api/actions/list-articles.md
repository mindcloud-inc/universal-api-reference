# List Articles with Usedesk

Retrieves a list of knowledge base articles from Usedesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/support/:account_id/articles/list`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [List Articles](https://api.usedocs.com/article/51399)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Knowledge base ID in the system. |
| `article_ids` | query | `string` | no | Article IDs, separated by commas. |
| `category_ids` | query | `string` | no | Category IDs, separated by commas. |
| `collection_ids` | query | `string` | no | Section IDs, separated by commas. |
| `order` | query | `string` | no | Sort order: asc or desc. |
| `query` | query | `string` | no | Search string for article title and text. |
| `sort` | query | `string` | no | Sort field. |
| `type` | query | `string` | no | Filter by article visibility: public or private. |
| `count` | query | `number` | no | Number of articles per page. |
| `page` | query | `number` | no | Page number. |
| `short_text` | query | `number` | no | Return trimmed search results when query is provided. |
