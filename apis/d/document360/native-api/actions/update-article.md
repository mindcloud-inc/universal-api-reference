# Update Article with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Articles/:articleId/:langCode`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Update Article](https://apidocs.document360.com/apidocs/update-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `string` | yes | The ID of the article |
| `langCode` | path | `string` | yes | The language code of the article |
| `title` | body | `string` | no | The updated title |
| `content` | body | `string` | no | The updated article content |
| `category_id` | body | `string` | no | The destination category |
| `hidden` | body | `boolean` | no | Whether the article is hidden |
| `version_number` | body | `number` | no | The article version to update |
| `translation_option` | body | `number` | no | The translation status |
| `source` | body | `string` | no | Free text for reference |
| `order` | body | `number` | no | The updated position inside the category |
