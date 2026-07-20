# Search Site with GitBook

Finds content in a GitBook site by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:organizationId/sites/:siteId/search`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Search Site](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | — |
| `query` | body | `string` | yes | Search query text. Maximum length: 512. |
| `scope.currentSiteSpace` | body | `string` | no | Include a specific current site space when using the default search scope. |
| `scope.mode` | body | `string` | yes | Search in all sections and site spaces, or narrow the search with a different scope mode. |
| `scope.siteSpaceIds[]` | body | `array<string>` | no | Search only within the provided site spaces when using the specific search scope. Send multiple values as a array. |
| `siteId` | path | `string` | yes | — |
