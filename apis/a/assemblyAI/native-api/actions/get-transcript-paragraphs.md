# Get Transcript Paragraphs with AssemblyAI

Retrieves paragraph segments from an AssemblyAI transcript.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript/:transcript_id/paragraphs`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Get Transcript Paragraphs](https://www.assemblyai.com/docs/api-reference/transcripts/get-paragraphs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | path | `string` | yes | The transcript ID to retrieve paragraphs for. |
