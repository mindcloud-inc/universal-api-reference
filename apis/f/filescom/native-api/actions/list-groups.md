# List Groups with Files.com

Retrieves group records from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Groups](https://developers.files.com/rest/resources/user-accounts/groups#list-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_parent_site_groups` | query | `boolean` | no | Include groups inherited from the parent site. |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
