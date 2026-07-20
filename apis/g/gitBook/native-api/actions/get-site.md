# Get Site with GitBook

Retrieves a site's details from GitBook.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/sites/:siteId`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Get Site](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `siteId` | path | `string` | yes |
