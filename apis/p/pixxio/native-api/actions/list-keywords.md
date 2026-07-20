# List Keywords with pixx.io

Retrieves keywords from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/keywords`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Keywords](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exactMatch` | query | `boolean` | no | Whether the keyword name filter must match exactly. |
| `name` | query | `string` | no | Filter keywords by name. |
