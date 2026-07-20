# List Login History with Files.com

Retrieves site login history from Files.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/history/login`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Login History](https://developers.files.com/rest/resources/logging/actions/#list-site-login-history)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor token returned by a previous login-history response page. |
| `display` | query | `string` | no | Optional display mode. Files.com supports `full` or `parent`. |
| `end_at` | query | `date` | no | Return login history entries at or before this timestamp. |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `per_page` | query | `string` | no | Maximum number of login history entries to return in one page. |
| `start_at` | query | `date` | no | Return login history entries at or after this timestamp. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
