# Better Proposals: Native API Reference

A consolidated summary of Better Proposals's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://betterproposals.io/resources/api/
- **API base URL:** `https://api.betterproposals.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Bptoken: <apiKey>
```

[Official authentication documentation](https://betterproposals.io/resources/api/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /company/create` | [docs](https://betterproposals.io/resources/api/) |
| [Create Document Type](actions/create-document-type.md) | `POST /doctype/create` | [docs](https://betterproposals.io/resources/api/) |
| [Create Proposal](actions/create-proposal.md) | `POST /proposal/create` | [docs](https://betterproposals.io/resources/api/) |
| [Create Proposal Cover](actions/create-proposal-cover.md) | `POST /proposal/cover/create` | [docs](https://betterproposals.io/resources/api/) |
| [Create Quote](actions/create-quote.md) | `POST /quote/create` | [docs](https://betterproposals.io/resources/api/) |
| [Get Brand Settings](actions/get-brand-settings.md) | `GET /settings/brand` | [docs](https://betterproposals.io/resources/api/) |
| [Get Company Details](actions/get-company-details.md) | `GET /company/:COMPANY_ID` | [docs](https://betterproposals.io/resources/api/) |
| [Get Currency Details](actions/get-currency-details.md) | `GET /currency/:CURRENCY_ID` | [docs](https://betterproposals.io/resources/api/) |
| [Get Custom Merge Tags](actions/get-custom-merge-tags.md) | `GET /settings/merge_tag` | [docs](https://betterproposals.io/resources/api/) |
| [Get Proposal Details](actions/get-proposal-details.md) | `GET /proposal/:PROPOSAL_ID` | [docs](https://betterproposals.io/resources/api/) |
| [Get Quote Details](actions/get-quote-details.md) | `GET /quote/:QUOTE_ID` | [docs](https://betterproposals.io/resources/api/) |
| [Get Settings](actions/get-settings.md) | `GET /settings` | [docs](https://betterproposals.io/resources/api/) |
| [Get Template Details](actions/get-template-details.md) | `GET /template/:TEMPLATE_ID` | [docs](https://betterproposals.io/resources/api/) |
| [List Companies](actions/list-companies.md) | `GET /company` | [docs](https://betterproposals.io/resources/api/) |
| [List Currencies](actions/list-currencies.md) | `GET /currency` | [docs](https://betterproposals.io/resources/api/) |
| [List Document Types](actions/list-document-types.md) | `GET /doctype` | [docs](https://betterproposals.io/resources/api/) |
| [List New Proposals](actions/list-new-proposals.md) | `GET /proposal/new` | [docs](https://betterproposals.io/resources/api/) |
| [List Opened Proposals](actions/list-opened-proposals.md) | `GET /proposal/opened` | [docs](https://betterproposals.io/resources/api/) |
| [List Proposals](actions/list-proposals.md) | `GET /proposal` | [docs](https://betterproposals.io/resources/api/) |
| [List Quotes](actions/list-quotes.md) | `GET /quote` | [docs](https://betterproposals.io/resources/api/) |
| [List Sent Proposals](actions/list-sent-proposals.md) | `GET /proposal/sent` | [docs](https://betterproposals.io/resources/api/) |
| [List Signed Proposals](actions/list-signed-proposals.md) | `GET /proposal/signed` | [docs](https://betterproposals.io/resources/api/) |
| [List Templates](actions/list-templates.md) | `GET /template` | [docs](https://betterproposals.io/resources/api/) |
