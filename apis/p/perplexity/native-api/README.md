# Perplexity: Native API Reference

A consolidated summary of Perplexity's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.perplexity.ai/docs/getting-started/quickstart
- **API base URL:** `https://api.perplexity.ai`

## Authentication

### API Key

Connect with a Perplexity API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.perplexity.ai/docs/getting-started/api-groups)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent Response](actions/create-agent-response.md) | `POST /v1/agent` | [docs](https://docs.perplexity.ai/api-reference/responses-post) |
| [Create Async Chat Completion](actions/create-async-chat-completion.md) | `POST /v1/async/sonar` | [docs](https://docs.perplexity.ai/api-reference/async-sonar-post) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/sonar` | [docs](https://docs.perplexity.ai/api-reference/sonar-post) |
| [Create Contextualized Embeddings](actions/create-contextualized-embeddings.md) | `POST /v1/contextualizedembeddings` | [docs](https://docs.perplexity.ai/api-reference/contextualized-embeddings-post) |
| [Create Embeddings](actions/create-embeddings.md) | `POST /v1/embeddings` | [docs](https://docs.perplexity.ai/api-reference/embeddings-post) |
| [Generate Auth Token](actions/generate-auth-token.md) | `POST /generate_auth_token` | [docs](https://docs.perplexity.ai/api-reference/generate-auth-token-post) |
| [Get Async Chat Completion](actions/get-async-chat-completion.md) | `GET /v1/async/sonar/:api_request` | [docs](https://docs.perplexity.ai/api-reference/async-sonar-api-request-get) |
| [List Async Chat Completions](actions/list-async-chat-completions.md) | `GET /v1/async/sonar` | [docs](https://docs.perplexity.ai/api-reference/async-sonar-get) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.perplexity.ai/api-reference/models-get) |
| [Revoke Auth Token](actions/revoke-auth-token.md) | `POST /revoke_auth_token` | [docs](https://docs.perplexity.ai/api-reference/revoke-auth-token-post) |
| [Search the Web](actions/search-the-web.md) | `POST /search` | [docs](https://docs.perplexity.ai/api-reference/search-post) |
