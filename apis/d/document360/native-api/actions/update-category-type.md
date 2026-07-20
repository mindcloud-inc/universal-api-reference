# Update Category Type with Document360

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/Categories/:categoryId/updateCategoryType`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Update Category Type](https://apidocs.document360.com/apidocs/update-the-category-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `categoryType` | query | `number` | yes | 0 Folder, 1 Page, 2 Index |
| `userId` | query | `string` | yes | The ID of the team account |
