# Grants.gov: Native API Reference

A consolidated summary of Grants.gov's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://grants.gov/api/api-guide
- **API base URL:** `https://api.grants.gov`

## Authentication

### Public REST API

Grants.gov public Applicant REST API endpoints do not require authentication for public opportunity search and detail retrieval.

This API does not require request authentication.

[Official authentication documentation](https://grants.gov/api/api-guide)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Opportunity](actions/fetch-opportunity.md) | `POST /v1/api/fetchOpportunity` | [docs](https://grants.gov/api/common/fetchopportunity) |
| [Search Opportunities](actions/search-opportunities.md) | `POST /v1/api/search2` | [docs](https://grants.gov/api/common/search2) |
