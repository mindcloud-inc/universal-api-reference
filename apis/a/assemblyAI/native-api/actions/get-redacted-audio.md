# Get Redacted Audio with AssemblyAI

Retrieves redacted audio details from an AssemblyAI transcript.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript/:transcript_id/redacted-audio`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Get Redacted Audio](https://www.assemblyai.com/docs/api-reference/transcripts/get-redacted-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | path | `string` | yes | ID of the transcript. |
