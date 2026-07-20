# Morph: Native API Reference

A consolidated summary of Morph's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.morphllm.com/introduction
- **API base URL:** `https://api.morphllm.com/v1`

## Authentication

### API Key

Use your Morph API key as a bearer token for the Morph API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.morphllm.com/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Code Changes](actions/apply-code-changes.md) | `POST /chat/completions` | [docs](https://docs.morphllm.com/api-reference/endpoint/apply) |
| [Compact Context](actions/compact-context.md) | `POST /compact` | [docs](https://docs.morphllm.com/api-reference/endpoint/compact) |
| [Generate Embedding](actions/generate-embedding.md) | `POST /embeddings` | [docs](https://docs.morphllm.com/api-reference/endpoint/embedding) |
| [Rerank Documents](actions/rerank-documents.md) | `POST /rerank` | [docs](https://docs.morphllm.com/api-reference/endpoint/rerank) |
| [Search Code With WarpGrep](actions/search-code-with-warp-grep.md) | `POST /chat/completions` | [docs](https://docs.morphllm.com/api-reference/endpoint/warpgrep) |
| [Verify API Key](actions/verify-api-key.md) | `POST /embeddings` | [docs](https://docs.morphllm.com/api-reference/endpoint/embedding) |
