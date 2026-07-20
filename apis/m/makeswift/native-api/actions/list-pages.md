# List Pages with Makeswift

Retrieves pages for a site from Makeswift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/pages`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [List Pages](https://docs.makeswift.com/developer/reference/api/pages/list-pages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | The site ID to list pages from. |
| `limit` | query | `number` | no | Maximum number of pages to return (1-100). |
| `startingAfter` | query | `string` | no | Pagination cursor ID. |
| `locale` | query | `string` | no | Filter pages by locale. |
| `pathPrefix` | query | `string` | no | Filter pages by pathname prefix. |
| `includeOffline` | query | `boolean` | no | Include offline pages when true. |
| `sortBy` | query | `string` | no | Sort field. |
| `sortDirection` | query | `string` | no | Sort direction. |
| `versionRef` | query | `string` | no | Use this version reference for content reads. |
