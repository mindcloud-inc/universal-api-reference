# List Files with pixx.io

Retrieves files from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Files](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeArchived` | query | `boolean` | no | Whether to include archived files. |
| `responseFields` | query | `string` | no | File fields to include in the response. Send multiple values as a array. |
| `semanticQuery` | query | `string` | no | Semantic search query for files. |
| `showFiles` | query | `boolean` | no | Whether to include file objects in the response. |
