# Generate Dubbed Video V2 with Pipio

Creates a dubbed video in Pipio using the v2 workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://project.pipio.ai/project/generate/dubbing/v2`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [Generate Dubbed Video V2](https://docs.pipio.ai/dubbing-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceUrl` | body | `string` | yes | The URL to your source video that will be dubbed. |
| `targetLanguage` | body | `string` | yes | Language code to translate and dub the video into. |
| `sourceLanguage` | body | `string` | no | Language code of the source video, or auto for automatic detection. |
