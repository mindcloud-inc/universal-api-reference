# List Site Spaces with GitBook

Retrieves spaces attached to a GitBook site.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:organizationId/sites/:siteId/site-spaces`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Site Spaces](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `default` | query | `boolean` | no |
| `organizationId` | path | `string` | yes |
| `shareKey` | query | `string` | no |
| `siteId` | path | `string` | yes |
