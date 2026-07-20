# Didit: Native API Reference

A consolidated summary of Didit's API configuration and 44 documented operations, with links to official documentation.

- **Official docs:** https://docs.didit.me/api-reference/overview
- **API base URL:** `https://verification.didit.me/v3`

## Authentication

### API Key

Use your Didit API key from API & Webhooks.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.didit.me/getting-started/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429`. Wait 5000 ms before the first retry. Stop after 4 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (44 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add to Blocklist](actions/add-to-blocklist.md) | `POST /blocklist/add/` | [docs](https://docs.didit.me/sessions-api/blocklist/add) |
| [Age Estimation](actions/age-estimation.md) | `POST https://verification.didit.me/v3/age-estimation/` | [docs](https://docs.didit.me/standalone-apis/age-estimation) |
| [AML Screening](actions/aml-screening.md) | `POST https://verification.didit.me/v3/aml/` | [docs](https://docs.didit.me/standalone-apis/aml-screening) |
| [Batch Delete Sessions](actions/batch-delete-sessions.md) | `POST /sessions/delete/` | [docs](https://docs.didit.me/management-api/sessions/batch-delete) |
| [Batch Delete Users](actions/batch-delete-users.md) | `POST /users/delete/` | [docs](https://docs.didit.me/management-api/users/delete) |
| [Check Email Code](actions/check-email-code.md) | `POST https://verification.didit.me/v3/email/check/` | [docs](https://docs.didit.me/standalone-apis/email-check) |
| [Check Phone Code](actions/check-phone-code.md) | `POST https://verification.didit.me/v3/phone/check/` | [docs](https://docs.didit.me/standalone-apis/phone-check) |
| [Create Questionnaire](actions/create-questionnaire.md) | `POST /questionnaires/` | [docs](https://docs.didit.me/management-api/questionnaires/create) |
| [Create Session](actions/create-session.md) | `POST https://verification.didit.me/v3/session/` | [docs](https://docs.didit.me/sessions-api/create-session) |
| [Create Session Review](actions/create-session-review.md) | `POST /sessions/{sessionId}/reviews/` | [docs](https://docs.didit.me/management-api/sessions/create-review) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows/` | [docs](https://docs.didit.me/management-api/workflows/create) |
| [Database Validation](actions/database-validation.md) | `POST https://verification.didit.me/v3/database-validation/` | [docs](https://docs.didit.me/standalone-apis/database-validation) |
| [Delete Questionnaire](actions/delete-questionnaire.md) | `DELETE /questionnaires/{questionnaireId}/` | [docs](https://docs.didit.me/management-api/questionnaires/delete) |
| [Delete Session](actions/delete-session.md) | `DELETE https://verification.didit.me/v3/session/{sessionId}/delete/` | [docs](https://docs.didit.me/sessions-api/delete-session) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflows/{workflowId}/` | [docs](https://docs.didit.me/management-api/workflows/delete) |
| [Face Match](actions/face-match.md) | `POST https://verification.didit.me/v3/face-match/` | [docs](https://docs.didit.me/standalone-apis/face-match) |
| [Face Search](actions/face-search.md) | `POST https://verification.didit.me/v3/face-search/` | [docs](https://docs.didit.me/standalone-apis/face-search) |
| [Generate Session PDF](actions/generate-session-pdf.md) | `GET https://verification.didit.me/v3/session/{sessionId}/generate-pdf` | [docs](https://docs.didit.me/sessions-api/generate-pdf) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /billing/balance/` | [docs](https://docs.didit.me/management-api/billing/balance) |
| [Get Questionnaire](actions/get-questionnaire.md) | `GET /questionnaires/{questionnaireId}/` | [docs](https://docs.didit.me/management-api/questionnaires/get) |
| [Get User](actions/get-user.md) | `GET /users/{vendorData}/` | [docs](https://docs.didit.me/management-api/users/get) |
| [Get Webhook Configuration](actions/get-webhook-configuration.md) | `GET /webhook/` | [docs](https://docs.didit.me/management-api/webhook/get) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/{workflowId}/` | [docs](https://docs.didit.me/management-api/workflows/get) |
| [ID Verification](actions/id-verification.md) | `POST https://verification.didit.me/v3/id-verification/` | [docs](https://docs.didit.me/standalone-apis/id-verification) |
| [Import Shared Session](actions/import-shared-session.md) | `POST https://verification.didit.me/v3/session/import-shared/` | [docs](https://docs.didit.me/sessions-api/share-session/import) |
| [List Blocklist](actions/list-blocklist.md) | `GET /blocklist/` | [docs](https://docs.didit.me/sessions-api/blocklist/list) |
| [List Questionnaires](actions/list-questionnaires.md) | `GET /questionnaires/` | [docs](https://docs.didit.me/management-api/questionnaires/list) |
| [List Session Reviews](actions/list-session-reviews.md) | `GET /sessions/{sessionId}/reviews/` | [docs](https://docs.didit.me/management-api/sessions/list-reviews) |
| [List Sessions](actions/list-sessions.md) | `GET https://verification.didit.me/v3/sessions` | [docs](https://docs.didit.me/sessions-api/list-sessions) |
| [List Users](actions/list-users.md) | `GET /users/` | [docs](https://docs.didit.me/management-api/users/list) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows/` | [docs](https://docs.didit.me/management-api/workflows/list) |
| [Passive Liveness](actions/passive-liveness.md) | `POST https://verification.didit.me/v3/passive-liveness/` | [docs](https://docs.didit.me/standalone-apis/passive-liveness) |
| [Proof of Address](actions/proof-of-address.md) | `POST https://verification.didit.me/v3/poa/` | [docs](https://docs.didit.me/standalone-apis/proof-of-address) |
| [Remove from Blocklist](actions/remove-from-blocklist.md) | `POST /blocklist/remove/` | [docs](https://docs.didit.me/sessions-api/blocklist/remove) |
| [Retrieve Session](actions/retrieve-session.md) | `GET https://verification.didit.me/v3/session/{sessionId}/decision/` | [docs](https://docs.didit.me/sessions-api/retrieve-session) |
| [Send Email Code](actions/send-email-code.md) | `POST https://verification.didit.me/v3/email/send/` | [docs](https://docs.didit.me/standalone-apis/email-send) |
| [Send Phone Code](actions/send-phone-code.md) | `POST https://verification.didit.me/v3/phone/send/` | [docs](https://docs.didit.me/standalone-apis/phone-send) |
| [Share Session](actions/share-session.md) | `POST https://verification.didit.me/v3/session/{sessionId}/share/` | [docs](https://docs.didit.me/sessions-api/share-session/share) |
| [Top Up Credits](actions/top-up-credits.md) | `POST /billing/top-up/` | [docs](https://docs.didit.me/management-api/billing/top-up) |
| [Update Questionnaire](actions/update-questionnaire.md) | `PATCH /questionnaires/{questionnaireId}/` | [docs](https://docs.didit.me/management-api/questionnaires/update) |
| [Update Session Status](actions/update-session-status.md) | `PATCH https://verification.didit.me/v3/session/{sessionId}/update-status/` | [docs](https://docs.didit.me/sessions-api/update-status) |
| [Update User](actions/update-user.md) | `PATCH /users/{vendorData}/` | [docs](https://docs.didit.me/management-api/users/update) |
| [Update Webhook Configuration](actions/update-webhook-configuration.md) | `PATCH /webhook/` | [docs](https://docs.didit.me/management-api/webhook/update) |
| [Update Workflow](actions/update-workflow.md) | `PATCH /workflows/{workflowId}/` | [docs](https://docs.didit.me/management-api/workflows/update) |
