# List Permission Groups with pixx.io

Retrieves permission groups from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/permissionGroups`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Permission Groups](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isAdmin` | query | `boolean` | no | Filter admin permission groups. |
| `isExternal` | query | `boolean` | no | Filter external permission groups. |
| `isReadOnly` | query | `boolean` | no | Filter read-only permission groups. |
| `searchTerm` | query | `string` | no | Search permission groups by term. |
