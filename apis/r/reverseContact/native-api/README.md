# Reverse Contact: Native API Reference

A consolidated summary of Reverse Contact's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.reversecontact.com/docs/endpoints
- **API base URL:** `https://api.reversecontact.com`

## Authentication

### API Key

Authenticate Reverse Contact API requests with an rc_ API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.reversecontact.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `data.metadata.pageNumber`. The current page number is read from `data.metadata.currentPage`.

## Pagination

Use `perPage` in the request body to set the page size (default 100; accepted range 1–100). Use `page` in the request body to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Company Profile Status](actions/check-company-profile-status.md) | `POST /v2/fetch/companies/check` | [docs](https://app.reversecontact.com/docs/endpoints/check-company) |
| [Check Person Profile Status](actions/check-person-profile-status.md) | `POST /v2/fetch/persons/check` | [docs](https://app.reversecontact.com/docs/endpoints/check-person) |
| [Fetch Company Posts](actions/fetch-company-posts.md) | `POST /v2/fetch/companies/posts/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-company-posts) |
| [Fetch Company Profile](actions/fetch-company-profile.md) | `POST /v2/fetch/companies` | [docs](https://app.reversecontact.com/docs/endpoints/fetch-company) |
| [Fetch Company Profile Live](actions/fetch-company-profile-live.md) | `POST /v2/fetch/companies/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-company) |
| [Fetch Person Comments](actions/fetch-person-comments.md) | `POST /v2/fetch/persons/comments/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-person-activity) |
| [Fetch Person Posts](actions/fetch-person-posts.md) | `POST /v2/fetch/persons/posts/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-person-activity) |
| [Fetch Person Profile](actions/fetch-person-profile.md) | `POST /v2/fetch/persons` | [docs](https://app.reversecontact.com/docs/endpoints/enrich-profile) |
| [Fetch Person Profile Live](actions/fetch-person-profile-live.md) | `POST /v2/fetch/persons/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-profile) |
| [Fetch Person Reactions](actions/fetch-person-reactions.md) | `POST /v2/fetch/persons/reactions/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-person-activity) |
| [Fetch Post Comments](actions/fetch-post-comments.md) | `POST /v2/fetch/posts/comments/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-post-comments) |
| [Fetch Post Details](actions/fetch-post-details.md) | `POST /v2/fetch/post/live` | [docs](https://app.reversecontact.com/docs/endpoints/live-post) |
| [Find Professional Email](actions/find-professional-email.md) | `POST /v2/contact/email` | [docs](https://app.reversecontact.com/docs/endpoints/contact-email) |
| [Get Usage](actions/get-usage.md) | `GET /v2/usage` | [docs](https://app.reversecontact.com/docs/endpoints/usage) |
| [Resolve Company From Domain](actions/resolve-company-from-domain.md) | `POST /v2/resolve/companies/live` | [docs](https://app.reversecontact.com/docs/endpoints/resolve-company) |
| [Resolve Person From Email](actions/resolve-person-from-email.md) | `POST /v2/resolve/persons/email` | [docs](https://app.reversecontact.com/docs/endpoints/resolve-person-email) |
| [Resolve Person From Name](actions/resolve-person-from-name.md) | `POST /v2/resolve/persons/name` | [docs](https://app.reversecontact.com/docs/endpoints/resolve-person-name) |
| [Search Companies](actions/search-companies.md) | `POST /v2/search/companies` | [docs](https://app.reversecontact.com/docs/endpoints/search-companies) |
| [Search Persons](actions/search-persons.md) | `POST /v2/search/persons` | [docs](https://app.reversecontact.com/docs/endpoints/search-persons) |
| [Verify Email](actions/verify-email.md) | `POST /v2/contact/email/verify` | [docs](https://app.reversecontact.com/docs/endpoints/contact-email-verify) |
