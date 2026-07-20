# List Bundles with Files.com

Retrieves share links from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/bundles`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Bundles](https://developers.files.com/rest/resources/sharing/share-links/bundles#list-share-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
