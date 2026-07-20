# Create Model with Fish Audio

Creates a new voice model in Fish Audio.

## Endpoint

- **Method:** `POST`
- **Path:** `/model`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [Create Model](https://docs.fish.audio/api-reference/endpoint/model/create-model)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visibility` | body | `list` | no | Whether the model is public, unlisted, or private. Accepted values: `0`, `1`, `2`. |
| `title` | body | `string` | yes | Model title or name. |
| `description` | body | `string` | no | Model description. |
| `cover_image` | body | `file` | no | Optional cover image. Required by Fish Audio when visibility is public. |
| `voices[]` | body | `array<file>` | yes | One or more voice audio files used to create the model. |
| `texts[]` | body | `array<string>` | no | Optional transcripts aligned to the uploaded voice files. |
| `tags[]` | body | `array<string>` | no | Optional model tags. |
| `enhance_audio_quality` | body | `boolean` | no | When true, Fish Audio enhances uploaded audio quality. |
