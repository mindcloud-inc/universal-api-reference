# Create Job with Temi

Creates a transcription job in Temi.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.temi.com/v1`
- **Official documentation:** [Create Job](https://www.temi.com/api/reference/v1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_url` | body | `string` | yes | Public URL of the audio or video file to transcribe. |
| `callback_url` | body | `string` | no | Optional URL Temi should call when the job completes or fails. |
| `metadata` | body | `string` | no | Optional metadata to associate with the submitted job. |
