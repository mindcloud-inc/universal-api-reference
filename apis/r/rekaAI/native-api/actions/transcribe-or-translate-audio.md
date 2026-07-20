# Transcribe or Translate Audio with Reka AI

Creates an audio transcription or translation in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/transcription_or_translation`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Transcribe or Translate Audio](https://docs.reka.ai/speech/api-reference/transcribe-or-translate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Audio file URL or data URI |
| `sampling_rate` | body | `number` | yes | Audio sampling rate in Hz |
