# Get Article by Version with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/Articles/:articleId/:langCode/versions/:versionNumber`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Get Article by Version](https://apidocs.document360.com/apidocs/get-article-by-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleId` | path | `string` | yes | The ID of the article |
| `langCode` | path | `string` | yes | The language code of the article |
| `versionNumber` | path | `number` | yes | The version number of the article |
| `isForDisplay` | query | `boolean` | no | Expand snippets and variables for display |
| `appendSASToken` | query | `boolean` | no | Whether to append SAS tokens for images and files |
