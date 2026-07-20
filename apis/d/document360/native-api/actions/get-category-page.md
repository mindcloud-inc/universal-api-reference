# Get Category Page with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Categories/:categoryId/content/:langCode`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Get Category Page](https://apidocs.document360.com/apidocs/get-category-page-with-an-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | The ID of the category |
| `langCode` | path | `string` | yes | The language code of the category |
| `isForDisplay` | query | `boolean` | no | Expand snippets and variables for display |
| `isPublished` | query | `boolean` | no | Whether to fetch the latest published category page |
| `appendSASToken` | query | `boolean` | no | Whether to append SAS tokens for images and files |
