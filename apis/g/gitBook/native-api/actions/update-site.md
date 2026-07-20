# Update Site with GitBook

Updates an existing site in GitBook.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orgs/:organizationId/sites/:siteId`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Update Site](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `basename` | body | `string` | no | — |
| `defaultLevel` | body | `string` | no | Default level applied to the site. |
| `defaultSiteSection` | body | `string` | no | — |
| `defaultSiteSpace` | body | `string` | no | — |
| `organizationId` | path | `string` | yes | — |
| `permissionsModel` | body | `string` | no | — |
| `siteId` | path | `string` | yes | — |
| `title` | body | `string` | no | Title of the site. Maximum length: 128. |
| `visibility` | body | `string` | no | — |
