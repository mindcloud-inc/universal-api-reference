# Update Category Page Content with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Categories/:categoryId/content/:langCode`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Update Category Page Content](https://apidocs.document360.com/apidocs/update-a-category-page-content-with-the-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `langCode` | path | `string` | yes | Language code of the category |
| `title` | body | `string` | no | Updated category page title |
| `content` | body | `string` | no | Updated category page content |
| `version_number` | body | `number` | no | Specific version number to update |
| `translation_option` | body | `string` | no | Translation status override |
| `source` | body | `string` | no | Free text source reference |
| `updated_by` | body | `string` | no | Team account ID responsible for the update |
