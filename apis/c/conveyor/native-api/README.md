# Conveyor: Native API Reference

A consolidated summary of Conveyor's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.conveyor.com/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/22yh3lmekbaq6v
- **API base URL:** `https://api.conveyor.com/api`

## Authentication

### API Key

Connect Conveyor using an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.conveyor.com/reference/api-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer Single Question](actions/answer-single-question.md) | `POST /v2/single_question` | [docs](https://docs.conveyor.com/reference/post-single-question) |
| [Create Authorization](actions/create-authorization.md) | `POST /v2/exchange/authorizations` | [docs](https://docs.conveyor.com/reference/post-authorization) |
| [Create Document](actions/create-document.md) | `POST /v2/exchange/documents` | [docs](https://docs.conveyor.com/reference/post-document) |
| [Create Folder](actions/create-folder.md) | `POST /v2/exchange/folders` | [docs](https://docs.conveyor.com/reference/post-folder) |
| [Create Questionnaire](actions/create-questionnaire.md) | `POST /v2/questionnaires` | [docs](https://docs.conveyor.com/reference/post-questionnaires) |
| [Create Questionnaire Request](actions/create-questionnaire-request.md) | `POST /v2/questionnaire_requests` | [docs](https://docs.conveyor.com/reference/post-questionnaire-requests) |
| [Create Review](actions/create-review.md) | `POST /v2/reviews` | [docs](https://docs.conveyor.com/reference/post-reviews) |
| [Delete Document](actions/delete-document.md) | `DELETE /v2/exchange/documents/:document_id` | [docs](https://docs.conveyor.com/reference/delete-document) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /v2/exchange/folders/:folder_id` | [docs](https://docs.conveyor.com/reference/delete-folder) |
| [Get Authorization Request](actions/get-authorization-request.md) | `GET /v2/exchange/authorization_requests/:authorization_request_id` | [docs](https://docs.conveyor.com/reference/get-authorization-request) |
| [Ignore Authorization Request](actions/ignore-authorization-request.md) | `PATCH /v2/exchange/authorization_requests/:authorization_request_id` | [docs](https://docs.conveyor.com/reference/patch-authorization-request) |
| [List Access Groups](actions/list-access-groups.md) | `GET /v2/exchange/access_groups` | [docs](https://docs.conveyor.com/reference/get-access-groups) |
| [List Authorization Requests](actions/list-authorization-requests.md) | `GET /v2/exchange/authorization_requests` | [docs](https://docs.conveyor.com/reference/get-authorization-requests) |
| [List Authorizations](actions/list-authorizations.md) | `GET /v2/exchange/authorizations` | [docs](https://docs.conveyor.com/reference/get-authorizations) |
| [List Connections](actions/list-connections.md) | `GET /v2/exchange/connections` | [docs](https://docs.conveyor.com/reference/get-connections) |
| [List Documents](actions/list-documents.md) | `GET /v2/exchange/documents` | [docs](https://docs.conveyor.com/reference/get-documents) |
| [List Folders](actions/list-folders.md) | `GET /v2/exchange/folders` | [docs](https://docs.conveyor.com/reference/get-folders) |
| [List Interactions](actions/list-interactions.md) | `GET /v2/interactions` | [docs](https://docs.conveyor.com/reference/get-interactions) |
| [List Interactions By Connection](actions/list-interactions-by-connection.md) | `GET /v2/interactions/connections/:connection_id` | [docs](https://docs.conveyor.com/reference/get-interactions-by-connection-id) |
| [List Interactions By Document](actions/list-interactions-by-document.md) | `GET /v2/interactions/documents/:document_id` | [docs](https://docs.conveyor.com/reference/get-interactions-by-document-id) |
| [List Interactions By Question](actions/list-interactions-by-question.md) | `GET /v2/interactions/questions/:question_id` | [docs](https://docs.conveyor.com/reference/get-interactions-by-question-id) |
| [List Knowledge Base Questions](actions/list-knowledge-base-questions.md) | `GET /v2/knowledge_base/questions` | [docs](https://docs.conveyor.com/reference/get-knowledge-base-questions) |
| [List Open Authorization Requests](actions/list-open-authorization-requests.md) | `GET /v2/exchange/authorization_request_queue` | [docs](https://docs.conveyor.com/reference/get-authorization-requests-queue) |
| [List Product Lines](actions/list-product-lines.md) | `GET /v2/product_lines` | [docs](https://docs.conveyor.com/reference/get-product-lines) |
| [List Questionnaires](actions/list-questionnaires.md) | `GET /v2/questionnaires` | [docs](https://docs.conveyor.com/reference/get-questionnaires) |
| [Update Authorization](actions/update-authorization.md) | `PATCH /v2/exchange/authorizations/:authorization_id` | [docs](https://docs.conveyor.com/reference/patch-authorization) |
| [Update Document](actions/update-document.md) | `PATCH /v2/exchange/documents/:document_id` | [docs](https://docs.conveyor.com/reference/patch-document) |
