# Import Knowledge Base Categories with Product Fruits

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/knowledgebase/categories/import`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Import Knowledge Base Categories](https://help.productfruits.com/en/article/knowledge-base-api-import-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories[]` | body | `array<object>` | yes | Array of category objects to import or update. |
| `config.articleHandling` | body | `string` | no | Reserved import category handling mode; currently documented as error. |
| `config.slugConflictHandling` | body | `string` | no | How to handle slug conflicts: error or auto-number. |
