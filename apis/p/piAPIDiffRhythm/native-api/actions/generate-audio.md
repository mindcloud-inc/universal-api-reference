# Generate Audio with PiAPI/DiffRhythm

Creates a DiffRhythm audio task in PiAPI/DiffRhythm.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Audio](https://piapi.ai/docs/diffrhythm-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_type` | body | `string` | yes | Choose `txt2audio-base` for shorter generations or `txt2audio-full` for longer songs. |
| `input.lyrics` | body | `string` | yes | Timed lyrics in DiffRhythm format such as `[00:10.00] line of lyrics`. |
| `input.style_prompt` | body | `string` | no | Describe the musical style, genre, or mood when you are not using a reference audio file. |
| `input.style_audio` | body | `string` | no | Optional reference audio URL or Base64 string to guide the generated style. |
| `config.webhook_config.endpoint` | body | `string` | no | Optional webhook URL for PiAPI task completion callbacks. |
| `config.webhook_config.secret` | body | `string` | no | Optional secret that PiAPI includes when calling your webhook. |
