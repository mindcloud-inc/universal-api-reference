# ProPublica Nonprofit Explorer: Native API Reference

A consolidated summary of ProPublica Nonprofit Explorer's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://projects.propublica.org/nonprofits/api/
- **API base URL:** `https://projects.propublica.org/nonprofits/api/v2`

## Authentication

### No authentication

ProPublica Nonprofit Explorer's public API accepts GET requests without authentication.

This API does not require request authentication.

[Official authentication documentation](https://projects.propublica.org/nonprofits/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | `GET /organizations/{{ein}}.json` | [docs](https://projects.propublica.org/nonprofits/api/) |
| [Search Organizations](actions/search-organizations.md) | `GET /search.json` | [docs](https://projects.propublica.org/nonprofits/api/) |
