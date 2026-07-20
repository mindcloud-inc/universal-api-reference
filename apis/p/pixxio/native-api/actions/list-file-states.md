# List File States with pixx.io

Retrieves file states from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/fileStates`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List File States](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isArchive` | query | `boolean` | no | Filter archive file states. |
| `name` | query | `string` | no | Filter file states by name. |
