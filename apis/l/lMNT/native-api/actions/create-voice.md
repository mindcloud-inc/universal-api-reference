# Create Voice with LMNT

Creates a new voice in LMNT.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/voice`
- **Base URL:** `https://api.lmnt.com`
- **Official documentation:** [Create Voice](https://docs.lmnt.com/api-reference/voice/create-voice)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the new voice. |
| `enhance` | body | `boolean` | yes | Whether LMNT should apply enhancement to noisy source audio. |
| `files` | body | `file` | yes | One or more training audio files in wav, mp3, mp4, m4a, or webm format. Send multiple values as a array. |
| `gender` | body | `string` | no | Optional gender tag such as male, female, or nonbinary. |
| `name` | body | `string` | yes | The display name for the new voice. |
