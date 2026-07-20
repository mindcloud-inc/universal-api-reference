# Text To Speech with TypeCast

Creates a speech audio file in TypeCast.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text-to-speech`
- **Base URL:** `https://api.typecast.ai/`
- **Official documentation:** [Text To Speech](https://typecast.ai/docs/api-reference/text-to-speech/text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | body | `list` | yes | TypeCast voice identifier to synthesize with. |
| `text` | body | `string` | yes | Text to convert to speech. Maximum length: 2000. |
| `model` | body | `list` | yes | TTS model version to use. Accepted values: `ssfm-v21`, `ssfm-v30`. |
| `language` | body | `string` | no | ISO 639-3 language code for synthesis. Maximum length: 3. |
| `prompt` | body | `object` | no | Emotion and style settings for the generated speech. |
| `prompt.emotion_type` | body | `list` | no | Prompt mode for emotion control. Accepted values: `preset`, `smart`. |
| `prompt.emotion_preset` | body | `list` | no | Emotion preset to apply. Accepted values: `angry`, `happy`, `normal`, `sad`, `tonedown`, `toneup`, `whisper`. |
| `prompt.emotion_intensity` | body | `number` | no | Strength of the emotional expression. |
| `prompt.previous_text` | body | `string` | no | Text that comes before the generated text for smart emotion inference. Maximum length: 2000. |
| `prompt.next_text` | body | `string` | no | Text that comes after the generated text for smart emotion inference. Maximum length: 2000. |
| `output` | body | `object` | no | Audio output settings for the generated speech. |
| `output.target_lufs` | body | `number` | no | Target loudness for normalized audio output. |
| `output.volume` | body | `number` | no | Relative output volume from 0 to 200. |
| `output.audio_pitch` | body | `number` | no | Pitch shift in semitones. |
| `output.audio_tempo` | body | `number` | no | Speech speed multiplier. |
| `output.audio_format` | body | `list` | no | Output audio format. Accepted values: `mp3`, `wav`. |
| `seed` | body | `number` | no | Random seed for speech variation. |
