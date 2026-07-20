# List Automations with Files.com

Retrieves automations from a Files.com site.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [List Automations](https://developers.files.com/rest/resources/automations/automations#list-automations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `per_page` | query | `number` | no | Maximum number of items to return in one page. |
| `cursor` | query | `string` | no | Cursor token returned by a previous page. |
