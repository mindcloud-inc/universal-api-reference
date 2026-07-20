# Convert Text to Audio with Dify

Creates audio from text in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-audio`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Convert Text to Audio](https://docs.dify.ai/api-reference/tts/convert-text-to-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | body | `string` | no | Message ID to convert to audio. |
| `text` | body | `string` | no | Text content to convert to audio. |
| `user` | body | `string` | no | User identifier. |
| `voice` | body | `string` | no | Voice to use for text-to-speech. |
| `streaming` | body | `boolean` | no | Whether to enable streaming audio response. |
