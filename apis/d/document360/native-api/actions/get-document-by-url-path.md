# Get Document by URL Path with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Project/Document`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Get Document by URL Path](https://apidocs.document360.com/apidocs/get-a-document-article-or-category-by-url-path)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The relative URL path |
| `applyRedirection` | query | `boolean` | no | Whether to apply active redirection rules |
| `isForDisplay` | query | `boolean` | no | Expand snippets and variables for display |
| `isPublished` | query | `boolean` | no | Whether to fetch the latest published version |
| `appendSASToken` | query | `boolean` | no | Whether to append SAS tokens for images and files |
