# Speech is Cheap: Native API Reference

A consolidated summary of Speech is Cheap's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.speechischeap.com/
- **API base URL:** `https://api.speechischeap.com/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.speechischeap.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Transcription Job](actions/cancel-transcription-job.md) | `DELETE /jobs/:job_id` | [docs](https://docs.speechischeap.com/jobs-v2/delete/) |
| [Create Transcription Job](actions/create-transcription-job.md) | `POST /jobs/` | [docs](https://docs.speechischeap.com/jobs-v2/create/) |
| [Get API Health](actions/get-api-health.md) | `GET /jobs/health` | [docs](https://docs.speechischeap.com/jobs-v2/health/) |
| [Get Transcription Job](actions/get-transcription-job.md) | `GET /jobs/:job_id` | [docs](https://docs.speechischeap.com/jobs-v2/read/) |
