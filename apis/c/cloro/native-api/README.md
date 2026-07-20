# Cloro: Native API Reference

A consolidated summary of Cloro's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloro.dev
- **API base URL:** `https://api.cloro.dev`

## Authentication

### API Key

Authenticate requests with a Cloro API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cloro.dev/guides/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Async Task](actions/create-async-task.md) | `POST /v1/async/task` | [docs](https://docs.cloro.dev/api-reference/endpoint/create-async-task) |
| [Create Batch Tasks](actions/create-batch-tasks.md) | `POST /v1/async/task/batch` | [docs](https://docs.cloro.dev/api-reference/endpoint/create-batch-tasks) |
| [Extract ChatGPT](actions/extract-chatgpt.md) | `POST /v1/monitor/chatgpt` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-chatgpt) |
| [Extract Google AI Mode](actions/extract-google-ai-mode.md) | `POST /v1/monitor/aimode` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-aimode) |
| [Extract Google AI Overview](actions/extract-google-ai-overview.md) | `POST /v1/monitor/google` | [docs](https://docs.cloro.dev/api-reference/endpoint/google/ai-overview) |
| [Extract Google Gemini](actions/extract-google-gemini.md) | `POST /v1/monitor/gemini` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-gemini) |
| [Extract Google News](actions/extract-google-news.md) | `POST /v1/monitor/google/news` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-google-news) |
| [Extract Google Search](actions/extract-google-search.md) | `POST /v1/monitor/google` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-google) |
| [Extract Grok](actions/extract-grok.md) | `POST /v1/monitor/grok` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-grok) |
| [Extract Microsoft Copilot](actions/extract-microsoft-copilot.md) | `POST /v1/monitor/copilot` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-copilot) |
| [Extract Perplexity](actions/extract-perplexity.md) | `POST /v1/monitor/perplexity` | [docs](https://docs.cloro.dev/api-reference/endpoint/monitor-perplexity) |
| [Get Async Status](actions/get-async-status.md) | `GET /v1/async/status` | [docs](https://docs.cloro.dev/api-reference/endpoint/get-async-status) |
| [Get Task Status](actions/get-task-status.md) | `GET /v1/async/task/:taskId` | [docs](https://docs.cloro.dev/api-reference/endpoint/get-task-status) |
| [List Countries](actions/list-countries.md) | `GET /v1/countries` | [docs](https://docs.cloro.dev/api-reference/endpoint/countries) |
