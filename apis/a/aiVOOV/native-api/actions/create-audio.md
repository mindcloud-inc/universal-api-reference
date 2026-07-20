# Create Audio with AiVOOV

Creates audio from multiple voice and text inputs in AiVOOV.

## Endpoint

- **Method:** `POST`
- **Path:** `/create`
- **Base URL:** `https://aivoov.com/api/v8`
- **Official documentation:** [Create Audio](https://github.com/AiVOOV/aivoov-api#create-audio-with-multiple-voice-and-text-inputs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | body | `list<string>` | yes | Select one or more voice IDs to synthesize. Send multiple values as a array. |
| `transcribe_text[]` | body | `array<string>` | yes | Enter the text for each selected voice in matching order. |
| `transcribe_ssml_pitch_rate[]` | body | `array<string>` | no | Optional pitch adjustment for each text item, or default. |
| `transcribe_ssml_spk_rate[]` | body | `array<string>` | no | Optional speaking-rate adjustment for each text item, or default. |
| `transcribe_ssml_volume[]` | body | `array<string>` | no | Optional volume adjustment for each text item, or default. |
