# TestDome: Native API Reference

A consolidated summary of TestDome's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs
- **OpenAPI specification:** https://api.staging.testdome.com/v3/openapi
- **API base URL:** `https://api.staging.testdome.com/v3`

## Authentication

### OAuth 2.0

Authenticate with TestDome using OAuth2 client credentials from the Integrations & API page.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.staging.testdome.com/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://www.testdome.com/integrations/api)

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–100). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Candidates](actions/archive-candidates.md) | `POST /candidates/archive` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Archive Test](actions/archive-test.md) | `POST /tests/:testId/archive` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Cancel Candidate Invite](actions/cancel-candidate-invite.md) | `POST /candidates/:candidateId/cancel-invite` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Create Candidate Sharing URL](actions/create-candidate-sharing-url.md) | `POST /candidates/:candidateId/sharing-url` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Create Test Candidates Share URL](actions/create-test-candidates-share-url.md) | `POST /tests/:testId/candidates/share-url` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Create Test URL](actions/create-test-url.md) | `POST /tests/:testId/urls` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Delete Test](actions/delete-test.md) | `DELETE /tests/:testId` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Extend Test Candidate Deadline](actions/extend-test-candidate-deadline.md) | `PUT /tests/:testId/candidates/deadline` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Get Candidate](actions/get-candidate.md) | `GET /candidates/:candidateId` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Get Current Plan](actions/get-current-plan.md) | `GET /accounts/current/plan` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Get Test](actions/get-test.md) | `GET /tests/:testId` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Get Test Settings](actions/get-test-settings.md) | `GET /tests/:testId/settings` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Invite Candidates Via Email](actions/invite-candidates-via-email.md) | `POST /tests/:testId/candidates/invite-via-email` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [List Test Candidates](actions/list-test-candidates.md) | `GET /tests/:testId/candidates` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [List Tests](actions/list-tests.md) | `GET /tests` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Notify Test Candidates](actions/notify-test-candidates.md) | `POST /tests/:testId/candidates/notify` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Provide Test Proctoring Consent](actions/provide-test-proctoring-consent.md) | `PUT /tests/:testId/candidates/proctoring-consent` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Unarchive Candidates](actions/unarchive-candidates.md) | `POST /candidates/unarchive` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Unarchive Test](actions/unarchive-test.md) | `POST /tests/:testId/unarchive` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Update Test Cutoff Score](actions/update-test-cutoff-score.md) | `PATCH /tests/:testId/cutoff-score` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Update Test Settings](actions/update-test-settings.md) | `PATCH /tests/:testId/settings` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Update Test URL](actions/update-test-url.md) | `PATCH /tests/:testId/urls/:testUrlId` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
| [Update Test URL Settings](actions/update-test-url-settings.md) | `PATCH /tests/:testId/url-settings` | [docs](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs) |
