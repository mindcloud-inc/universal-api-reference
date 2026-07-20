# List Collections with pixx.io

Retrieves collections from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Collections](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isDynamic` | query | `boolean` | no | Filter collections by dynamic/static status. |
| `searchTerm` | query | `string` | no | Search collections by term. |
| `withFileID` | query | `number` | no | Return collections containing the given file ID. |
