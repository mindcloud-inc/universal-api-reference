# List Categories in Project Version with Document360

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/ProjectVersions/:projectVersionId/categories`
- **Base URL:** `https://apihub.document360.io`
- **Official documentation:** [List Categories in Project Version](https://apidocs.document360.com/apidocs/project-version-categories)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectVersionId` | path | `string` | yes |
| `excludeArticles` | query | `boolean` | no |
| `langCode` | query | `string` | no |
| `includeCategoryDescription` | query | `boolean` | no |
| `securityVisibility` | query | `number` | no |
