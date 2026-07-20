# Update Category with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Categories/:categoryId`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Update Category](https://apidocs.document360.com/apidocs/update-a-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `name` | body | `string` | no | Updated category name |
| `order` | body | `number` | no | Updated sort order |
| `parent_category_id` | body | `string` | no | Move the category under a different parent |
| `hidden` | body | `boolean` | no | Whether the category is hidden |
| `icon` | body | `string` | no | Unicode icon for the category |
| `language` | body | `string` | no | Language code to update |
