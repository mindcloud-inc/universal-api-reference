# List Directories with pixx.io

Retrieves directories from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/directories`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Directories](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter directories by name. |
| `permission` | query | `string` | no | Filter directories by permission. |
| `showSubVersions` | query | `boolean` | no | Whether to show subversion files. |
