# BuildBetter: Native API Reference

A consolidated summary of BuildBetter's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.buildbetter.ai/pages/api
- **API base URL:** `https://api.buildbetter.app/v1`

## Authentication

### API Key

Use your BuildBetter organization API key to authenticate GraphQL requests.

### Credentials

- **API Key:** `apiKey` · required
- **Organization Key:** `organizationKey` · optional · Optional when your BuildBetter account requires explicit organization selection.

Send these headers with each API request:

```http
X-Buildbetter-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.buildbetter.ai/pages/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-companies) |
| [Create Person](actions/create-person.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-and-editing-profiles) |
| [Get Call By ID](actions/get-call-by-id.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#calls-interviews) |
| [Get Call Details With Participants](actions/get-call-details-with-participants.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#calls-interviews) |
| [Get Call Transcript](actions/get-call-transcript.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#get-call-transcript) |
| [Get Company By ID](actions/get-company-by-id.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-profile) |
| [Get Document By ID](actions/get-document-by-id.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#get-document-details) |
| [Get Person By ID](actions/get-person-by-id.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#person-profile-features) |
| [Get Signal By ID](actions/get-signal-by-id.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [List Calls by Date Range](actions/list-calls-by-date-range.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#search-calls) |
| [List Calls by Participant Email](actions/list-calls-by-participant-email.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#filtering) |
| [List Calls Paginated](actions/list-calls-paginated.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-examples#offset-pagination) |
| [List Companies](actions/list-companies.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-management) |
| [List Conversations](actions/list-conversations.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/Organization/conversations-messaging) |
| [List Documents](actions/list-documents.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#documents) |
| [List Folders](actions/list-folders.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/Organization/collections-overview) |
| [List People](actions/list-people.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#get-people) |
| [List People by Company](actions/list-people-by-company.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#finding-people) |
| [List Recent Calls](actions/list-recent-calls.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#get-recent-calls) |
| [List Recent Signals](actions/list-recent-signals.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [List Signals by Date Range](actions/list-signals-by-date-range.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [List Signals by Sentiment](actions/list-signals-by-sentiment.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [List Signals by Type](actions/list-signals-by-type.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [List Signals for Call](actions/list-signals-for-call.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#get-call-signals) |
| [Search Calls By Title](actions/search-calls-by-title.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/graphql-queries#search-calls) |
| [Search Companies By Name Or Domain](actions/search-companies-by-name-or-domain.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-search) |
| [Search People By Name](actions/search-people-by-name.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#finding-people) |
| [Search Signals By Summary Phrase](actions/search-signals-by-summary-phrase.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions) |
| [Update Company](actions/update-company.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-properties) |
| [Update Person](actions/update-person.md) | `POST /graphql` | [docs](https://docs.buildbetter.ai/pages/CRM%20Integration/people-and-companies#creating-and-editing-profiles) |
