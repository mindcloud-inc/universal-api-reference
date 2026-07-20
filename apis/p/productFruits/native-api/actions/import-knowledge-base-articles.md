# Import Knowledge Base Articles with Product Fruits

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/knowledgebase/import`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Import Knowledge Base Articles](https://help.productfruits.com/en/article/knowledge-base-api-import-articles-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articles[]` | body | `array<object>` | yes | Array of article objects to import or update. |
| `config.ignoreImportErrors` | body | `boolean` | no | Allow partial imports by ignoring non-serious errors. |
| `config.includeContentInResponse` | body | `boolean` | no | Include full content details in the import response. |
| `config.slugConflictHandling` | body | `string` | no | How to handle slug conflicts: error or auto-number. |
