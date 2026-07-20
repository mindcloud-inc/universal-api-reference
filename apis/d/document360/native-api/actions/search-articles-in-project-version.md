# Search Articles in Project Version with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ProjectVersions/:projectVersionId/:langCode`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [Search Articles in Project Version](https://apidocs.document360.com/apidocs/search-inside-project-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectVersionId` | path | `string` | yes | The project version ID |
| `langCode` | path | `string` | yes | The language code |
| `searchQuery` | query | `string` | yes | The phrase to search for |
| `page` | query | `number` | no | Page number, zero-based |
| `hitsPerPage` | query | `number` | no | Number of hits per page |
