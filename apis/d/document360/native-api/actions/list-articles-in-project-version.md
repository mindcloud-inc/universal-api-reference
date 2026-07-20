# List Articles in Project Version with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ProjectVersions/:projectVersionId/articles`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [List Articles in Project Version](https://apidocs.document360.com/apidocs/project-version-articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectVersionId` | path | `string` | yes | The project version ID |
| `langCode` | query | `string` | no | Optional language code for filtering articles by language |
| `page` | query | `number` | no | Page number, zero-based |
| `hitsPerPage` | query | `number` | no | Number of results per page |
| `securityVisibility` | query | `number` | no | Optional protection level filter |
