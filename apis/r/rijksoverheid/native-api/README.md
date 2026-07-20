# Rijksoverheid: Native API Reference

A consolidated summary of Rijksoverheid's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.rijksoverheid.nl/opendata
- **API base URL:** `https://opendata.rijksoverheid.nl`

## Authentication

### No Authentication

Rijksoverheid open-data endpoints used by this app are public and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.rijksoverheid.nl/opendata/schoolvakanties)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get School Holidays By School Year](actions/get-school-holidays-by-school-year.md) | `GET /v1/infotypes/schoolholidays/schoolyear/{{schoolYear}}` | [docs](https://www.rijksoverheid.nl/opendata/schoolvakanties) |
| [List School Holidays](actions/list-school-holidays.md) | `GET /v1/infotypes/schoolholidays` | [docs](https://www.rijksoverheid.nl/opendata/schoolvakanties) |
