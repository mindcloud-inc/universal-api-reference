# Create Forced Alignment with ElevenLabs

Creates forced alignment data from audio in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/forced-alignment`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Forced Alignment](https://elevenlabs.io/docs/api-reference/forced-alignment/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio file to align. |
| `text` | body | `string` | yes | — |
| `enabled_spooled_file` | body | `boolean` | no | Stream large files in chunks. |
