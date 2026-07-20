# US Congress CRS: Native API Reference

A consolidated summary of US Congress CRS's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md
- **API base URL:** `https://api.congress.gov/v3`

## Authentication

### API Key

Use a Congress.gov API key issued through api.data.gov.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/LibraryOfCongress/api.congress.gov#keys)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–250). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get CRS Report](actions/get-crs-report.md) | `GET /crsreport/:reportNumber` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md) |
| [List CRS Reports](actions/list-crs-reports.md) | `GET /crsreport` | [docs](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md) |
