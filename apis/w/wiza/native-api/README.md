# Wiza: Native API Reference

A consolidated summary of Wiza's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.wiza.co
- **API base URL:** `https://wiza.co/api`

## Authentication

### ApiKey

Authenticate to Wiza by sending your API key in the Authorization header as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required · Your Wiza API key. MindCloud sends it as the Authorization Bearer token in the Authorization header.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.wiza.co/using-the-api/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Company Enrichment](actions/company-enrichment.md) | `POST /company_enrichments` | [docs](https://docs.wiza.co/api-reference/company-enrichment/company-enrichment) |
| [Continue Prospect Search](actions/continue-prospect-search.md) | `POST /prospects/continue_search` | [docs](https://docs.wiza.co/api-reference/prospect-lists/continue-prospect-search) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://docs.wiza.co/api-reference/lists/create-list) |
| [Create Prospect List](actions/create-prospect-list.md) | `POST /prospects/create_prospect_list` | [docs](https://docs.wiza.co/api-reference/prospect-lists/create-prospect-list) |
| [Get Credits](actions/get-credits.md) | `GET /meta/credits` | [docs](https://docs.wiza.co/api-reference/credits/get-credits) |
| [Get Individual Reveal](actions/get-individual-reveal.md) | `GET /individual_reveals/:id` | [docs](https://docs.wiza.co/api-reference/individual-reveals/get-individual-reveal) |
| [Get List](actions/get-list.md) | `GET /lists/:id` | [docs](https://docs.wiza.co/api-reference/lists/get-list) |
| [Get List Contacts](actions/get-list-contacts.md) | `GET /lists/:id/contacts` | [docs](https://docs.wiza.co/api-reference/lists/get-list-contacts) |
| [Prospect Search](actions/prospect-search.md) | `POST /prospects/search` | [docs](https://docs.wiza.co/api-reference/prospect/prospect-search) |
| [Start Individual Reveal](actions/start-individual-reveal.md) | `POST /individual_reveals` | [docs](https://docs.wiza.co/api-reference/individual-reveals/start-individual-reveal) |
