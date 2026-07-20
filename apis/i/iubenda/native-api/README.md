# iubenda: Native API Reference

A consolidated summary of iubenda's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/
- **API base URL:** `https://consent.iubenda.com`

## Authentication

### API Key

Use the iubenda Consent Database private API key for HTTP API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100).

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Consent](actions/create-consent.md) | `POST /consent` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent) |
| [Create Document](actions/create-document.md) | `POST /beta/documents` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#document) |
| [Create Legal Notice](actions/create-legal-notice.md) | `POST /legal_notices` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices) |
| [Create Subject](actions/create-subject.md) | `POST /subjects` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects) |
| [Get Consent](actions/get-consent.md) | `GET /consent/:id` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent) |
| [Get Document](actions/get-document.md) | `GET /beta/documents/:id` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#document) |
| [Get Latest Consent for Subject](actions/get-latest-consent-for-subject.md) | `GET /beta/subjects/:id/consent/last` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent) |
| [Get Legal Notice Version](actions/get-legal-notice-version.md) | `GET /legal_notices/:identifier/:version` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices) |
| [Get Subject](actions/get-subject.md) | `GET /subjects/:id` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects) |
| [List Consents](actions/list-consents.md) | `GET /consent` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#consent) |
| [List Documents](actions/list-documents.md) | `GET /beta/documents` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#document) |
| [List Legal Notice Versions](actions/list-legal-notice-versions.md) | `GET /legal_notices/:identifier` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices) |
| [List Legal Notices](actions/list-legal-notices.md) | `GET /legal_notices` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#legal-notices) |
| [List Subjects](actions/list-subjects.md) | `GET /subjects` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects) |
| [Update Subject](actions/update-subject.md) | `PATCH /subjects/:id` | [docs](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#subjects) |
