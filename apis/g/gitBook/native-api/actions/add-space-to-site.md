# Add Space To Site with GitBook

Adds an existing space to a GitBook site.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:organizationId/sites/:siteId/site-spaces`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Add Space To Site](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `draft` | body | `boolean` | no |
| `organizationId` | path | `string` | yes |
| `sectionId` | body | `string` | no |
| `siteId` | path | `string` | yes |
| `spaceId` | body | `string` | yes |
