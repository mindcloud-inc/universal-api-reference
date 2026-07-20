# Get Transcript Sentences with AssemblyAI

Retrieves sentence segments from an AssemblyAI transcript.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript/:transcript_id/sentences`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Get Transcript Sentences](https://www.assemblyai.com/docs/api-reference/transcripts/get-sentences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | path | `string` | yes | The transcript ID to retrieve sentences for. |
