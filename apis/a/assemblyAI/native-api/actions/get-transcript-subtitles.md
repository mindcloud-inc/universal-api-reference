# Get Transcript Subtitles with AssemblyAI

Retrieves subtitle text for an AssemblyAI transcript.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript/:transcript_id/:subtitle_format`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Get Transcript Subtitles](https://www.assemblyai.com/docs/api-reference/transcripts/get-subtitles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | path | `string` | yes | The transcript ID to export subtitles for. |
| `subtitle_format` | path | `string` | yes | Subtitle format to export. |
| `chars_per_caption` | query | `number` | no | Maximum characters per subtitle caption. |
