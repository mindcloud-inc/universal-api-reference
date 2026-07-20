# Vectara: Native API Reference

A consolidated summary of Vectara's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.vectara.com/docs/rest-api
- **OpenAPI specification:** https://docs.vectara.com/vectara-oas-v2.yaml
- **API base URL:** `https://api.vectara.io`

## Authentication

### OAuth 2.0

Vectara uses OAuth 2.0 client credentials for server-to-server authentication. Create an App Client in Vectara Console and paste the client ID and client secret into the connection form.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.vectara.io/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.vectara.com/docs/security/authentication/oauth-2)

## API conventions

Response data is read from `corpora`. The next-page cursor is read from `metadata.page_key`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100).

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | `POST /v2/corpora/:corpus_key/documents` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Advanced Single Corpus Query](actions/advanced-single-corpus-query.md) | `POST /v2/corpora/:corpus_key/query` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Correct Hallucinations](actions/correct-hallucinations.md) | `POST /v2/hallucination_correctors/correct_hallucinations` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v2/llms/chat/completions` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Create Corpus](actions/create-corpus.md) | `POST /v2/corpora` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Delete Corpus](actions/delete-corpus.md) | `DELETE /v2/corpora/:corpus_key` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Delete Document](actions/delete-document.md) | `DELETE /v2/corpora/:corpus_key/documents/:document_id` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Evaluate Factual Consistency](actions/evaluate-factual-consistency.md) | `POST /v2/evaluate_factual_consistency` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Get Corpus](actions/get-corpus.md) | `GET /v2/corpora/:corpus_key` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Get Document](actions/get-document.md) | `GET /v2/corpora/:corpus_key/documents/:document_id` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [List Corpora](actions/list-corpora.md) | `GET /v2/corpora` | [docs](https://docs.vectara.com/docs/rest-api/list-corpora) |
| [List Documents](actions/list-documents.md) | `GET /v2/corpora/:corpus_key/documents` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [List Encoders](actions/list-encoders.md) | `GET /v2/encoders` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [List Generation Presets](actions/list-generation-presets.md) | `GET /v2/generation_presets` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [List Jobs](actions/list-jobs.md) | `GET /v2/jobs` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [List Rerankers](actions/list-rerankers.md) | `GET /v2/rerankers` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Multi Corpora Query](actions/multi-corpora-query.md) | `POST /v2/query` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Query Metadata](actions/query-metadata.md) | `POST /v2/corpora/:corpus_key/metadata_query` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Replace Document Metadata](actions/replace-document-metadata.md) | `PUT /v2/corpora/:corpus_key/documents/:document_id/metadata` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Simple Single Corpus Query](actions/simple-single-corpus-query.md) | `GET /v2/corpora/:corpus_key/query` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Update Corpus](actions/update-corpus.md) | `PATCH /v2/corpora/:corpus_key` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Update Document](actions/update-document.md) | `PATCH /v2/corpora/:corpus_key/documents/:document_id` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
| [Upload File](actions/upload-file.md) | `POST /v2/corpora/:corpus_key/upload_file` | [docs](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2) |
