# Delete Article Content by Language with Product Fruits

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/knowledgebase/articles/:correlationId/content/:lang`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Delete Article Content by Language](https://help.productfruits.com/en/article/knowledge-base-api-delete-article--by-language-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `correlationId` | path | `string` | yes | The correlation ID of the article whose language content will be deleted. |
| `lang` | path | `string` | yes | ISO 639-1 language code of the content to delete. |
