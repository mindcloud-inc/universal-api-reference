# Search Transcript Words with AssemblyAI

Finds keywords in an AssemblyAI transcript.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transcript/:transcript_id/word-search`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Search Transcript Words](https://www.assemblyai.com/docs/api-reference/transcripts/word-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | path | `string` | yes | The transcript ID to search. |
| `words` | query | `string` | yes | One or more keywords to search for in the transcript. Send multiple values as a string separated by `,`. |
