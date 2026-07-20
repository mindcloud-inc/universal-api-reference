# <img src="https://images.mindcloud.co/apps/icons/cloro-logo_1778082884690.png" alt="Cloro logo" width="28" height="28"> Cloro: Universal API

Extract AI and search results into structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloro/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloro.dev
- **Vendor API docs:** https://docs.cloro.dev

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Async Queue Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Status](actions/get-async-status.md) | GET |  |

### Async Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Async Task](actions/create-async-task.md) | POST |  |
| [Get Task Status](actions/get-task-status.md) | GET |  |

### Async Task Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Tasks](actions/create-batch-tasks.md) | POST |  |

### Chatgpt Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract ChatGPT](actions/extract-chatgpt.md) | POST |  |

### Copilot Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract Microsoft Copilot](actions/extract-microsoft-copilot.md) | POST |  |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET |  |

### Gemini Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract Google Gemini](actions/extract-google-gemini.md) | POST |  |

### Google Ai Mode Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract Google AI Mode](actions/extract-google-ai-mode.md) | POST |  |

### Google Ai Overview

| Action | Method | Description |
| --- | --- | --- |
| [Extract Google AI Overview](actions/extract-google-ai-overview.md) | POST |  |

### Google News Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Google News](actions/extract-google-news.md) | POST |  |

### Google Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Google Search](actions/extract-google-search.md) | POST |  |

### Grok Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract Grok](actions/extract-grok.md) | POST |  |

### Perplexity Response

| Action | Method | Description |
| --- | --- | --- |
| [Extract Perplexity](actions/extract-perplexity.md) | POST |  |

