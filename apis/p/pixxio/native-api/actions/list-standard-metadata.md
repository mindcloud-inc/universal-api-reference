# List Standard Metadata with pixx.io

Retrieves standard metadata from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/metadata/standard`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Standard Metadata](https://api.pixxio.com/docs/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `number<number>` | no | Filter standard metadata by IDs. Send multiple values as a array. |
| `searchTerm` | query | `string` | no | Search standard metadata fields by term. |
