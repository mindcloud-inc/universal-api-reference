# List Knowledge Base Articles with Product Fruits

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/knowledgebase/articles`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [List Knowledge Base Articles](https://help.productfruits.com/en/article/knowledge-base-api-list-articles-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `correlationCategoryId` | query | `string` | no | Filter articles by category correlation ID. Omit for all articles or use null for uncategorized root articles. |
