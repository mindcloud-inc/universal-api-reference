# Rev AI: Native API Reference

A consolidated summary of Rev AI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.rev.ai
- **API base URL:** `https://api.rev.ai`

## Authentication

### API Key

Use a Rev AI access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.rev.ai/api/asynchronous)

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 1000). Use `starting_after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 2 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Vocabulary](actions/create-custom-vocabulary.md) | `POST /speechtotext/v1/vocabularies` | [docs](https://docs.rev.ai/api/custom-vocabulary/reference) |
| [Delete Custom Vocabulary](actions/delete-custom-vocabulary.md) | `DELETE /speechtotext/v1/vocabularies/:id` | [docs](https://docs.rev.ai/api/custom-vocabulary/reference) |
| [Delete Sentiment Analysis Job](actions/delete-sentiment-analysis-job.md) | `DELETE /sentiment_analysis/v1/jobs/:id` | [docs](https://docs.rev.ai/api/sentiment-analysis/reference) |
| [Delete Topic Extraction Job](actions/delete-topic-extraction-job.md) | `DELETE /topic_extraction/v1/jobs/:id` | [docs](https://docs.rev.ai/api/topic-extraction/reference) |
| [Delete Transcription Job](actions/delete-transcription-job.md) | `DELETE /speechtotext/v1/jobs/:id` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Account](actions/get-account.md) | `GET /speechtotext/v1/account` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Captions](actions/get-captions.md) | `GET /speechtotext/v1/jobs/:id/captions` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Custom Vocabulary](actions/get-custom-vocabulary.md) | `GET /speechtotext/v1/vocabularies/:id` | [docs](https://docs.rev.ai/api/custom-vocabulary/reference) |
| [Get Sentiment Analysis Job](actions/get-sentiment-analysis-job.md) | `GET /sentiment_analysis/v1/jobs/:id` | [docs](https://docs.rev.ai/api/sentiment-analysis/reference) |
| [Get Sentiment Analysis Result](actions/get-sentiment-analysis-result.md) | `GET /sentiment_analysis/v1/jobs/:id/result` | [docs](https://docs.rev.ai/api/sentiment-analysis/reference) |
| [Get Topic Extraction Job](actions/get-topic-extraction-job.md) | `GET /topic_extraction/v1/jobs/:id` | [docs](https://docs.rev.ai/api/topic-extraction/reference) |
| [Get Topic Extraction Result](actions/get-topic-extraction-result.md) | `GET /topic_extraction/v1/jobs/:id/result` | [docs](https://docs.rev.ai/api/topic-extraction/reference) |
| [Get Transcript](actions/get-transcript.md) | `GET /speechtotext/v1/jobs/:id/transcript` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Transcript Summary](actions/get-transcript-summary.md) | `GET /speechtotext/v1/jobs/:id/transcript/summary` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Transcription Job](actions/get-transcription-job.md) | `GET /speechtotext/v1/jobs/:id` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Translated Captions](actions/get-translated-captions.md) | `GET /speechtotext/v1/jobs/:id/captions/translation/:language` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Get Translated Transcript](actions/get-translated-transcript.md) | `GET /speechtotext/v1/jobs/:id/transcript/translation/:language` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [List Custom Vocabularies](actions/list-custom-vocabularies.md) | `GET /speechtotext/v1/vocabularies` | [docs](https://docs.rev.ai/api/custom-vocabulary/reference) |
| [List Sentiment Analysis Jobs](actions/list-sentiment-analysis-jobs.md) | `GET /sentiment_analysis/v1/jobs` | [docs](https://docs.rev.ai/api/sentiment-analysis/reference) |
| [List Topic Extraction Jobs](actions/list-topic-extraction-jobs.md) | `GET /topic_extraction/v1/jobs` | [docs](https://docs.rev.ai/api/topic-extraction/reference) |
| [List Transcription Jobs](actions/list-transcription-jobs.md) | `GET /speechtotext/v1/jobs` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
| [Submit Sentiment Analysis Job](actions/submit-sentiment-analysis-job.md) | `POST /sentiment_analysis/v1/jobs` | [docs](https://docs.rev.ai/api/sentiment-analysis/reference) |
| [Submit Topic Extraction Job](actions/submit-topic-extraction-job.md) | `POST /topic_extraction/v1/jobs` | [docs](https://docs.rev.ai/api/topic-extraction/reference) |
| [Submit Transcription Job](actions/submit-transcription-job.md) | `POST /speechtotext/v1/jobs` | [docs](https://docs.rev.ai/api/asynchronous/reference) |
