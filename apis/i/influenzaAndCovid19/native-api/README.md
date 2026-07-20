# Influenza and Covid-19: Native API Reference

A consolidated summary of Influenza and Covid-19's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://dev.socrata.com/docs/endpoints.html
- **API base URL:** `https://data.cdc.gov`

## Authentication

### No authentication

Public CDC Data.CDC.gov dataset reads do not require user credentials. Socrata application tokens are optional for higher throttling limits and are not required for these public read actions.

This API does not require request authentication.

[Official authentication documentation](https://dev.socrata.com/docs/app-tokens.html)

## Pagination

Use `$limit` in the query string to set the page size (default 100; accepted range 1–5000). Use `$offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gte`, `lte`.

## Sorting

Set the sort field with `$order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Emergency Department Respiratory Daily](actions/list-emergency-department-respiratory-daily.md) | `GET /resource/vjzj-u7u8.json` | [docs](https://data.cdc.gov/Coronavirus-and-Other-Respiratory-Viruses/NSSP-Emergency-Department-Respiratory-Daily/vjzj-u7u8/about_data) |
| [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md) | `GET /resource/7xva-uux8.json` | [docs](https://data.cdc.gov/Public-Health-Surveillance/NSSP-Emergency-Department-Visits-COVID-19-Flu-RSV-/7xva-uux8) |
| [List Provisional Respiratory Death Percentages](actions/list-provisional-respiratory-death-percentages.md) | `GET /resource/4bc2-bbpq.json` | [docs](https://data.cdc.gov/National-Center-for-Health-Statistics/Provisional-Percent-of-Deaths-for-COVID-19-Influen/4bc2-bbpq) |
| [List Viral Respiratory Test Positivity](actions/list-viral-respiratory-test-positivity.md) | `GET /resource/seuz-s2cv.json` | [docs](https://data.cdc.gov/Public-Health-Surveillance/Percent-of-Tests-Positive-for-Viral-Respiratory-Pa/seuz-s2cv) |
