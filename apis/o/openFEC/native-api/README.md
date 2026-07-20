# OpenFEC: Native API Reference

A consolidated summary of OpenFEC's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://api.open.fec.gov/developers/
- **OpenAPI specification:** https://api.open.fec.gov/swagger/
- **API base URL:** `https://api.open.fec.gov/v1`

## Authentication

### API Key

Authenticate requests with an OpenFEC API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.open.fec.gov/developers/)

## API conventions

Responses from this API use JSON. Response data is read from `results`. The total page count is read from `pagination.pages`. The current page number is read from `pagination.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Candidate Names](actions/find-candidate-names.md) | `GET /names/candidates/` | [docs](https://api.open.fec.gov/developers/) |
| [Find Committee Names](actions/find-committee-names.md) | `GET /names/committees/` | [docs](https://api.open.fec.gov/developers/) |
| [Get Candidate](actions/get-candidate.md) | `GET /candidate/:candidate_id/` | [docs](https://api.open.fec.gov/developers/) |
| [Get Committee](actions/get-committee.md) | `GET /committee/:committee_id/` | [docs](https://api.open.fec.gov/developers/) |
| [Get Disbursement](actions/get-disbursement.md) | `GET /schedules/schedule_b/:sub_id/` | [docs](https://api.open.fec.gov/developers/) |
| [Get Election Summary](actions/get-election-summary.md) | `GET /elections/summary/` | [docs](https://api.open.fec.gov/developers/) |
| [Get Itemized Receipt](actions/get-itemized-receipt.md) | `GET /schedules/schedule_a/:sub_id/` | [docs](https://api.open.fec.gov/developers/) |
| [List Calendar Dates](actions/list-calendar-dates.md) | `GET /calendar-dates/` | [docs](https://api.open.fec.gov/developers/) |
| [List Candidate Filings](actions/list-candidate-filings.md) | `GET /candidate/:candidate_id/filings/` | [docs](https://api.open.fec.gov/developers/) |
| [List Candidate History](actions/list-candidate-history.md) | `GET /candidate/:candidate_id/history/` | [docs](https://api.open.fec.gov/developers/) |
| [List Candidate Totals](actions/list-candidate-totals.md) | `GET /candidate/:candidate_id/totals/` | [docs](https://api.open.fec.gov/developers/) |
| [List Candidates](actions/list-candidates.md) | `GET /candidates/` | [docs](https://api.open.fec.gov/developers/) |
| [List Committee History](actions/list-committee-history.md) | `GET /committee/:committee_id/history/` | [docs](https://api.open.fec.gov/developers/) |
| [List Committee Reports](actions/list-committee-reports.md) | `GET /committee/:committee_id/reports/` | [docs](https://api.open.fec.gov/developers/) |
| [List Committee Totals](actions/list-committee-totals.md) | `GET /committee/:committee_id/totals/` | [docs](https://api.open.fec.gov/developers/) |
| [List Committees](actions/list-committees.md) | `GET /committees/` | [docs](https://api.open.fec.gov/developers/) |
| [List Disbursements](actions/list-disbursements.md) | `GET /schedules/schedule_b/` | [docs](https://api.open.fec.gov/developers/) |
| [List Disbursements By Recipient](actions/list-disbursements-by-recipient.md) | `GET /schedules/schedule_b/by_recipient/` | [docs](https://api.open.fec.gov/developers/) |
| [List Filings](actions/list-filings.md) | `GET /filings/` | [docs](https://api.open.fec.gov/developers/) |
| [List Independent Expenditures](actions/list-independent-expenditures.md) | `GET /schedules/schedule_e/` | [docs](https://api.open.fec.gov/developers/) |
| [List Itemized Receipts](actions/list-itemized-receipts.md) | `GET /schedules/schedule_a/` | [docs](https://api.open.fec.gov/developers/) |
| [List Receipts By Employer](actions/list-receipts-by-employer.md) | `GET /schedules/schedule_a/by_employer/` | [docs](https://api.open.fec.gov/developers/) |
| [List Receipts By Occupation](actions/list-receipts-by-occupation.md) | `GET /schedules/schedule_a/by_occupation/` | [docs](https://api.open.fec.gov/developers/) |
| [List Receipts By State](actions/list-receipts-by-state.md) | `GET /schedules/schedule_a/by_state/` | [docs](https://api.open.fec.gov/developers/) |
| [List Reports By Entity Type](actions/list-reports-by-entity-type.md) | `GET /reports/:entity_type/` | [docs](https://api.open.fec.gov/developers/) |
| [Search Candidates](actions/search-candidates.md) | `GET /candidates/search/` | [docs](https://api.open.fec.gov/developers/) |
| [Search Elections](actions/search-elections.md) | `GET /elections/search/` | [docs](https://api.open.fec.gov/developers/) |
| [Search Legal Documents](actions/search-legal-documents.md) | `GET /legal/search/` | [docs](https://api.open.fec.gov/developers/) |
