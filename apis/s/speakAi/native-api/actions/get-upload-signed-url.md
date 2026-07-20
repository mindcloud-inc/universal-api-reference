# Get Upload Signed URL with Speak Ai

Retrieves an upload signed URL from Speak Ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/media/upload/signedurl`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Get Upload Signed URL](https://docs.speakai.co/#24bd40af-fdb6-42e3-a89b-e55f7670db16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isVideo` | query | `boolean` | yes | Whether the upload target is a video file instead of audio. |
| `filename` | query | `string` | yes | Filename including the extension for the signed upload target. |
| `mimeType` | query | `string` | yes | File MIME type such as audio/mp3 or video/mp4. |
