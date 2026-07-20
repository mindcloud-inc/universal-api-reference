# List Users with Files.com

Retrieves user accounts from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Users](https://developers.files.com/rest/resources/user-accounts/users#list-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_parent_site_users` | query | `boolean` | no | Include users inherited from the parent site. |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
| `search` | query | `string` | no | Search users by text. |
