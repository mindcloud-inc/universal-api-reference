# Tomba: Native API Reference

A consolidated summary of Tomba's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.tomba.io/api
- **API base URL:** `https://api.tomba.io/v1`

## Authentication

### API Key

Connect to Tomba with an API key and API secret.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Required Tomba API secret used in the X-Tomba-Secret header. This value typically starts with ts_.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tomba.io/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 10–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Author Finder](actions/author-finder.md) | `GET /author-finder` | [docs](https://docs.tomba.io/api/finder#author-finder) |
| [Combined Enrichment](actions/combined-enrichment.md) | `GET /combined/find` | [docs](https://docs.tomba.io/api/enrichment#combined-api) |
| [Domain Search](actions/domain-search.md) | `GET /domain-search` | [docs](https://docs.tomba.io/api/finder#domain-search) |
| [Domain Status](actions/domain-status.md) | `GET /domain-status` | [docs](https://docs.tomba.io/api/~endpoints#domain-status) |
| [Email Count](actions/email-count.md) | `GET /email-count` | [docs](https://docs.tomba.io/api/finder#email-count) |
| [Email Enrichment](actions/email-enrichment.md) | `GET /enrich` | [docs](https://docs.tomba.io/api/finder#email-enrichment) |
| [Email Finder](actions/email-finder.md) | `GET /email-finder` | [docs](https://docs.tomba.io/api/finder#email-finder) |
| [Email Format](actions/email-format.md) | `GET /email-format` | [docs](https://docs.tomba.io/api/finder#email-format) |
| [Email Sources](actions/email-sources.md) | `GET /email-sources` | [docs](https://docs.tomba.io/api/~endpoints#email-sources) |
| [Email Verifier](actions/email-verifier.md) | `GET /email-verifier` | [docs](https://docs.tomba.io/api/verifier#email-verifier) |
| [Find Company](actions/find-company.md) | `GET /companies/find` | [docs](https://docs.tomba.io/api/enrichment#company-api) |
| [Find Person](actions/find-person.md) | `GET /people/find` | [docs](https://docs.tomba.io/api/enrichment#person-api) |
| [Get Account](actions/get-account.md) | `GET /me` | [docs](https://docs.tomba.io/api/account#get-account) |
| [Get Domain Suggestions](actions/get-domain-suggestions.md) | `GET /domain-suggestions` | [docs](https://docs.tomba.io/api/domain-suggestions#get-domain-suggestions) |
| [LinkedIn Finder](actions/linked-in-finder.md) | `GET /linkedin` | [docs](https://docs.tomba.io/api/finder#linkedin-finder) |
| [List Lead Lists](actions/list-lead-lists.md) | `GET /leads_lists` | [docs](https://docs.tomba.io/api/lead-lists#retrieve-leads-lists) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://docs.tomba.io/api/leads#retrieve-leads) |
| [Location](actions/location.md) | `GET /location` | [docs](https://docs.tomba.io/api/finder#location) |
| [Phone Finder](actions/phone-finder.md) | `GET /phone-finder` | [docs](https://docs.tomba.io/api/phone#phone-finder) |
| [Phone Validator](actions/phone-validator.md) | `GET /phone-validator` | [docs](https://docs.tomba.io/api/phone#phone-validator) |
| [Retrieve API Usage](actions/retrieve-api-usage.md) | `GET /usage` | [docs](https://docs.tomba.io/api/account#retrieve-api-usage) |
| [Search Companies](actions/search-companies.md) | `POST /reveal/search` | [docs](https://docs.tomba.io/api/reveal#search-companies) |
| [Similar Domains](actions/similar-domains.md) | `GET /similar` | [docs](https://docs.tomba.io/api/~endpoints#similar) |
| [Technology](actions/technology.md) | `GET /technology` | [docs](https://docs.tomba.io/api/~endpoints#technology) |
