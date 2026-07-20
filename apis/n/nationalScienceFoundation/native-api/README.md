# National Science Foundation: Native API Reference

A consolidated summary of National Science Foundation's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://resources.research.gov/common/webapi/awardapisearch-v1.htm
- **API base URL:** `https://api.nsf.gov/services/v1`

## Authentication

### No Auth

The NSF Award Search API is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://resources.research.gov/common/webapi/awardapisearch-v1.htm)

## API conventions

Responses from this API use JSON. Response data is read from `response.award`. The current page number is read from `response.metadata.offset`.

## Pagination

Use `rpp` in the query string to set the page size (default 25; accepted range 1–25). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sortKey` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Award](actions/get-award.md) | `GET /awards/[:id].json` | [docs](https://resources.research.gov/common/webapi/awardapisearch-v1.htm) |
| [Get Award Project Outcomes](actions/get-award-project-outcomes.md) | `GET /awards/[:id]/projectoutcomes.json` | [docs](https://resources.research.gov/common/webapi/awardapisearch-v1.htm) |
| [Search Awards](actions/search-awards.md) | `GET /awards.json` | [docs](https://resources.research.gov/common/webapi/awardapisearch-v1.htm) |
