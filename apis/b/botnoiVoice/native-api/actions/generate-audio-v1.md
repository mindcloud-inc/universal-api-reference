# Generate Audio V1 with Botnoi Voice

Generates audio with Botnoi Voice V1.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v1/generate_audio`
- **Base URL:** `https://api-voice.botnoi.ai`
- **Official documentation:** [Generate Audio V1](https://api-voice.botnoi.ai/openapi/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to convert into speech audio. |
| `speaker` | body | `string` | yes | Speaker identifier to use for voice generation. |
| `type_media` | body | `string` | yes | Output media format for the generated audio. |
| `volume` | body | `number` | no | Volume level for the generated audio. |
| `speed` | body | `number` | no | Playback speed for the generated audio. |
| `save_file` | body | `boolean` | no | Whether Botnoi should save the generated file. |
| `language` | body | `string` | no | Language code for synthesis. |
| `page` | body | `string` | no | Generation page context expected by the API. |
