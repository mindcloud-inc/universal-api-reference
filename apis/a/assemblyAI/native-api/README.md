# AssemblyAI: Native API Reference

A consolidated summary of AssemblyAI's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.assemblyai.com/docs/api-reference
- **OpenAPI specification:** https://raw.githubusercontent.com/AssemblyAI/assemblyai-api-spec/main/openapi.json
- **API base URL:** `https://api.assemblyai.com`

## Authentication

### API Key

Authenticate using an AssemblyAI API key sent in the Authorization request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.assemblyai.com/docs/api-reference/overview)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–200). Use `after_id` in the query string as the pagination cursor.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Transcript](actions/delete-transcript.md) | `DELETE /v2/transcript/:transcript_id` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/delete) |
| [Generate Temporary Streaming Token](actions/generate-temporary-streaming-token.md) | `GET https://streaming.assemblyai.com/v3/token` | [docs](https://www.assemblyai.com/docs/api-reference/streaming-api/generate-streaming-token) |
| [Get Redacted Audio](actions/get-redacted-audio.md) | `GET /v2/transcript/:transcript_id/redacted-audio` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/get-redacted-audio) |
| [Get Transcript](actions/get-transcript.md) | `GET /v2/transcript/:transcript_id` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/get) |
| [Get Transcript Paragraphs](actions/get-transcript-paragraphs.md) | `GET /v2/transcript/:transcript_id/paragraphs` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/get-paragraphs) |
| [Get Transcript Sentences](actions/get-transcript-sentences.md) | `GET /v2/transcript/:transcript_id/sentences` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/get-sentences) |
| [Get Transcript Subtitles](actions/get-transcript-subtitles.md) | `GET /v2/transcript/:transcript_id/:subtitle_format` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/get-subtitles) |
| [List Transcripts](actions/list-transcripts.md) | `GET /v2/transcript` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/list) |
| [Process Speech Understanding](actions/process-speech-understanding.md) | `POST https://llm-gateway.assemblyai.com/v1/understanding` | [docs](https://www.assemblyai.com/docs/api-reference/llm-gateway/create-speech-understanding) |
| [Search Transcript Words](actions/search-transcript-words.md) | `GET /v2/transcript/:transcript_id/word-search` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/word-search) |
| [Transcribe Audio](actions/transcribe-audio.md) | `POST /v2/transcript` | [docs](https://www.assemblyai.com/docs/api-reference/transcripts/submit) |
