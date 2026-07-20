# List Projects with Files.com

Retrieves projects from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Projects](https://developers.files.com/rest/resources/file-system/project-management/projects#list-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
