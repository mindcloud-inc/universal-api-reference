# List Requests with Files.com

Retrieves requests from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Requests](https://developers.files.com/rest/resources/file-system/requests/#list-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mine` | query | `boolean` | no | When true, return only requests owned by the current Files.com user. |
| `path` | query | `string` | no | Optional folder path to scope the request list. Send `/` to represent the site root. |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
