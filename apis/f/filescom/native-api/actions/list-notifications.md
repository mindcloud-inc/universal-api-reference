# List Notifications with Files.com

Retrieves notifications from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/notifications`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Notifications](https://developers.files.com/rest/resources/notifications/notifications/#list-notifications)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `number` | no | Optional group ID to scope notifications. |
| `include_ancestors` | query | `boolean` | no | When Path is set, include notifications inherited from parent paths. |
| `path` | query | `string` | no | Optional path to scope notifications. |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
