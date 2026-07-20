# Create Custom Voice with CAMB.AI

Creates a new custom voice in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-custom-voice`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Custom Voice](https://docs.camb.ai/api-reference/endpoint/create-custom-voice)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_name` | body | `string` | yes | Name to assign to the custom voice. |
| `gender` | body | `number` | yes | Gender code for the custom voice sample. |
| `file` | body | `file` | yes | Reference audio file used to create the custom voice. |
| `description` | body | `string` | no | Optional summary of the custom voice and its intended use. |
| `age` | body | `number` | no | Estimated or actual age of the speaker in the reference audio. |
| `enhance_audio` | body | `boolean` | no | Whether CAMB.AI should enhance the uploaded sample before cloning. |
| `language` | body | `number` | no | Optional numeric language identifier for the reference audio. |
