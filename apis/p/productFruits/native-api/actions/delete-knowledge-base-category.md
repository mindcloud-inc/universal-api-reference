# Delete Knowledge Base Category with Product Fruits

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/knowledgebase/categories/:correlationId`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Delete Knowledge Base Category](https://help.productfruits.com/en/article/knowledge-base-api-delete-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleHandling` | query | `string` | no | How to handle articles in deleted categories: error or move-to-root. |
| `correlationId` | path | `string` | yes | The correlation ID of the category to delete. |
