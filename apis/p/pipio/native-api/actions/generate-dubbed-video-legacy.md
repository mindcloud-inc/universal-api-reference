# Generate Dubbed Video Legacy with Pipio

Creates a dubbed video in Pipio using the legacy workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://project.pipio.ai/project/generate/dubbing`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [Generate Dubbed Video Legacy](https://docs.pipio.ai/generate-dubbed-video-tutorial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceLanguage` | body | `string` | no | Language code of the source video, or auto for automatic detection. |
| `targetLanguage` | body | `string` | yes | Language code to translate and dub the video into. |
| `sourceUrl` | body | `string` | yes | The URL to your source video that will be dubbed. |
| `voiceOnly` | body | `boolean` | no | Whether to generate translated audio only without lip sync. |
