# List Upload Links with pixx.io

Retrieves upload links from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/uploadLinks`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Upload Links](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `boolean` | no | Filter upload links by active status. |
| `name` | query | `string` | no | Filter upload links by name. |
| `userID` | query | `number` | no | Filter upload links by user ID. |
