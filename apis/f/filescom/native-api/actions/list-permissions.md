# List Permissions with Files.com

Retrieves permission records from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/permissions`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Permissions](https://developers.files.com/rest/resources/user-accounts/permissions#list-permissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
