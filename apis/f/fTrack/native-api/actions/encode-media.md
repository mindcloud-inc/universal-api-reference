# Encode Media with FTrack

Creates a media encoding job in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Encode Media](https://developer.ftrack.com/api/operations/encode-media-api-encode-media-encodemedia-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_id` | body | `string` | yes | Component to encode. |
| `keep_original` | body | `boolean` | yes | Whether to keep the original media after encoding. |
