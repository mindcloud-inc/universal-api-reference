# <img src="https://images.mindcloud.co/apps/icons/assembly-ai_1773587681521.png" alt="AssemblyAI logo" width="28" height="28"> AssemblyAI: Universal API

Speech-to-text, streaming transcription, speech understanding, and LLM Gateway APIs from AssemblyAI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assemblyAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assemblyai.com
- **Vendor API docs:** https://www.assemblyai.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transcripts](actions/list-transcripts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/list-transcripts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Llm Gateway

| Action | Method | Description |
| --- | --- | --- |
| [Process Speech Understanding](actions/process-speech-understanding.md) | POST | Creates speech understanding output from an AssemblyAI transcript. |

### Streaming

| Action | Method | Description |
| --- | --- | --- |
| [Generate Temporary Streaming Token](actions/generate-temporary-streaming-token.md) | GET | Retrieves a temporary streaming token from AssemblyAI. |

### Transcripts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transcript](actions/delete-transcript.md) | DELETE | Deletes one transcript from your AssemblyAI account. |
| [Get Redacted Audio](actions/get-redacted-audio.md) | GET | Retrieves redacted audio details from an AssemblyAI transcript. |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves one transcript from your AssemblyAI account. |
| [Get Transcript Paragraphs](actions/get-transcript-paragraphs.md) | GET | Retrieves paragraph segments from an AssemblyAI transcript. |
| [Get Transcript Sentences](actions/get-transcript-sentences.md) | GET | Retrieves sentence segments from an AssemblyAI transcript. |
| [Get Transcript Subtitles](actions/get-transcript-subtitles.md) | GET | Retrieves subtitle text for an AssemblyAI transcript. |
| [List Transcripts](actions/list-transcripts.md) | GET | Retrieves transcript records from your AssemblyAI account. |
| [Search Transcript Words](actions/search-transcript-words.md) | GET | Finds keywords in an AssemblyAI transcript. |
| [Transcribe Audio](actions/transcribe-audio.md) | POST | Creates a new transcript from a media URL in AssemblyAI. |

