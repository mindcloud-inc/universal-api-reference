# Sapling: Native API Reference

A consolidated summary of Sapling's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://sapling.ai/docs/api/
- **API base URL:** `https://api.sapling.ai`

## Authentication

### API Key

Use a Sapling API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sapling.ai/docs/api/api-access/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Completion](actions/accept-completion.md) | `POST /api/v1/complete/:completionId/accept` | [docs](https://sapling.ai/docs/api/autocomplete/) |
| [Add Custom Mapping](actions/add-custom-mapping.md) | `POST /api/v1/custom_mapping` | [docs](https://sapling.ai/docs/api/custom-mappings/) |
| [Add Dictionary Entry](actions/add-dictionary-entry.md) | `POST /api/v1/dictionary` | [docs](https://sapling.ai/docs/api/dictionary/) |
| [Analyze Sentiment](actions/analyze-sentiment.md) | `POST /api/v1/sentiment` | [docs](https://sapling.ai/docs/api/sentiment/) |
| [Detect AI-Generated Text](actions/detect-ai-generated-text.md) | `POST /api/v1/aidetect` | [docs](https://sapling.ai/docs/api/detector/) |
| [Detect Profanity](actions/detect-profanity.md) | `POST /api/v1/profanity` | [docs](https://sapling.ai/docs/api/profanity/) |
| [Detect Tone](actions/detect-tone.md) | `POST /api/v1/tone` | [docs](https://sapling.ai/docs/api/tone/) |
| [Expand Text](actions/expand-text.md) | `POST /api/v1/rephrase` | [docs](https://sapling.ai/docs/api/rephrase/) |
| [Formalize Text](actions/formalize-text.md) | `POST /api/v1/rephrase` | [docs](https://sapling.ai/docs/api/rephrase/) |
| [Get Autocomplete](actions/get-autocomplete.md) | `POST /api/v1/complete` | [docs](https://sapling.ai/docs/api/autocomplete/) |
| [Get Edits](actions/get-edits.md) | `POST /api/v1/edits` | [docs](https://sapling.ai/docs/api/edits-overview/) |
| [Get Similar Terms](actions/get-similar-terms.md) | `POST /api/v1/thesaurus` | [docs](https://sapling.ai/docs/api/similar-terms/) |
| [Get Spellcheck Suggestions](actions/get-spellcheck-suggestions.md) | `POST /api/v1/spellcheck` | [docs](https://sapling.ai/docs/api/spellcheck/) |
| [List Custom Mappings](actions/list-custom-mappings.md) | `GET /api/v1/custom_mapping` | [docs](https://sapling.ai/docs/api/custom-mappings/) |
| [List Dictionary Entries](actions/list-dictionary-entries.md) | `GET /api/v1/dictionary` | [docs](https://sapling.ai/docs/api/dictionary/) |
| [Remove Custom Mapping](actions/remove-custom-mapping.md) | `DELETE /api/v1/custom_mapping/:customMappingId` | [docs](https://sapling.ai/docs/api/custom-mappings/) |
| [Remove Dictionary Entry](actions/remove-dictionary-entry.md) | `DELETE /api/v1/dictionary/:dictionaryEntryId` | [docs](https://sapling.ai/docs/api/dictionary/) |
| [Rewrite in Active Voice](actions/rewrite-in-active-voice.md) | `POST /api/v1/rephrase` | [docs](https://sapling.ai/docs/api/rephrase/) |
| [Split Sentences](actions/split-sentences.md) | `POST /api/v1/rephrase` | [docs](https://sapling.ai/docs/api/rephrase/) |
| [Summarize Text](actions/summarize-text.md) | `POST /api/v1/summarize` | [docs](https://sapling.ai/docs/api/summarize/) |
