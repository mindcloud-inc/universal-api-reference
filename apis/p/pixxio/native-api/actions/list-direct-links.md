# List Direct Links with pixx.io

Retrieves direct links from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/directLinks`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Direct Links](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileIDs` | query | `number<number>` | no | Filter direct links by file IDs. Send multiple values as a array. |
| `fileName` | query | `string` | no | Filter direct links by file name. |
| `isCustom` | query | `boolean` | no | Filter by custom direct links. |
