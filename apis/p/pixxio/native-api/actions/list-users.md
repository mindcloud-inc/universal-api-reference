# List Users with pixx.io

Retrieves users from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Users](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `boolean` | no | Filter users by active status. |
| `permissionGroupIDs` | query | `number<number>` | no | Filter users by permission group IDs. Send multiple values as a array. |
| `searchTerm` | query | `string` | no | Search users by term. |
