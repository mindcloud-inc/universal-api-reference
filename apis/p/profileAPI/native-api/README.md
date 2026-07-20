# profileAPI: Native API Reference

A consolidated summary of profileAPI's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://documentation.profileapi.com/
- **API base URL:** `https://api.profileapi.com/2024-03-01`

## Authentication

### API Key

Authenticate requests with a profileAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documentation.profileapi.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company Find Job](actions/create-company-find-job.md) | `POST /companies/find/jobs` | [docs](https://documentation.profileapi.com/api-reference/create-company-find-job/) |
| [Find Companies](actions/find-companies.md) | `POST /companies/find` | [docs](https://documentation.profileapi.com/api-reference/find-companies/) |
| [Find Persons](actions/find-persons.md) | `POST /persons/find` | [docs](https://documentation.profileapi.com/api-reference/find-persons/) |
| [Get Company Find Job](actions/get-company-find-job.md) | `GET /companies/find/jobs/:jobId` | [docs](https://documentation.profileapi.com/api-reference/get-company-find-job/) |
| [Get Latest Company Find Job](actions/get-latest-company-find-job.md) | `GET /companies/find/jobs/latest` | [docs](https://documentation.profileapi.com/api-reference/get-latest-company-find-job/) |
| [List Company Find Jobs](actions/list-company-find-jobs.md) | `GET /companies/find/jobs` | [docs](https://documentation.profileapi.com/api-reference/list-company-find-jobs/) |
| [Lookup Email](actions/lookup-email.md) | `POST /email-contacts/lookup` | [docs](https://documentation.profileapi.com/api-reference/lookup-email/) |
| [Lookup Phone](actions/lookup-phone.md) | `POST /phone-contacts/lookup` | [docs](https://documentation.profileapi.com/api-reference/lookup-phone/) |
| [Reverse Lookup Email](actions/reverse-lookup-email.md) | `POST /email-contacts/reverse-lookup` | [docs](https://documentation.profileapi.com/api-reference/reverse-lookup-email/) |
| [Reverse Lookup Phone](actions/reverse-lookup-phone.md) | `POST /phone-contacts/reverse-lookup` | [docs](https://documentation.profileapi.com/api-reference/reverse-lookup-phone/) |
