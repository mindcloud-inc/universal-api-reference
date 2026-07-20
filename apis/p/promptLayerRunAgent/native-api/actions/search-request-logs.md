# Search Request Logs with PromptLayer Run Agent

Finds request logs in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/requests/search`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Search Request Logs](https://docs.promptlayer.com/reference/search-request-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | no | Free-text search query for request logs. |
| `include_prompt_name` | body | `boolean` | no | Whether to include prompt names in each search result. |
| `filter_group` | body | `object` | no | Structured filter group with nested AND or OR logic. |
| `page` | body | `number` | no | Page number for pagination. |
| `per_page` | body | `number` | no | Number of results per page. |
| `sort_by` | body | `list` | no | Field to sort request logs by. |
| `sort_order` | body | `list` | no | Sort direction to use with sortBy. |
