# Delete Article Content Version with Product Fruits

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/knowledgebase/articles/:correlationId/content/:lang/:id`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Delete Article Content Version](https://help.productfruits.com/en/article/knowledge-base-api-delete-article-content-version-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `correlationId` | path | `string` | yes | The correlation ID of the article. |
| `id` | path | `string` | yes | The correlation ID of the specific content version to delete. |
| `lang` | path | `string` | yes | ISO 639-1 language code of the content version. |
