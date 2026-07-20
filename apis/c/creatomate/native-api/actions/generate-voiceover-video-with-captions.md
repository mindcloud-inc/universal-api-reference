# Generate Voiceover Video With Captions with Creatomate

Creates a voiceover video with captions in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Generate Voiceover Video With Captions](https://creatomate.com/docs/api/quick-start/generate-a-voice-over-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voiceoverText` | body | `string` | yes | Text to synthesize into the voiceover audio. |
| `transcriptEffect` | body | `string` | no | Caption animation effect applied to the transcript. |
| `voiceProvider` | body | `string` | no | Creatomate provider string for the speech engine and voice selection. |
