# OpenPLZ: Native API Reference

A consolidated summary of OpenPLZ's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.openplzapi.org/en/api/
- **OpenAPI specification:** https://openplzapi.org/swagger/v1/swagger.json
- **API base URL:** `https://openplzapi.org`

## Authentication

### No authentication

OpenPLZ API is publicly accessible and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.openplzapi.org/en/faq/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `text/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Full Text Search Austria](actions/full-text-search-austria.md) | `GET /at/FullTextSearch` | [docs](https://www.openplzapi.org/en/austria/#requesting-streets) |
| [Full Text Search Germany](actions/full-text-search-germany.md) | `GET /de/FullTextSearch` | [docs](https://www.openplzapi.org/en/germany/#requesting-streets) |
| [Full Text Search Liechtenstein](actions/full-text-search-liechtenstein.md) | `GET /li/FullTextSearch` | [docs](https://www.openplzapi.org/en/liechtenstein/#requesting-streets) |
| [Full Text Search Switzerland](actions/full-text-search-switzerland.md) | `GET /ch/FullTextSearch` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-streets) |
| [List Austrian Districts by Federal Province](actions/list-austrian-districts-by-federal-province.md) | `GET /at/FederalProvinces/{key}/Districts` | [docs](https://www.openplzapi.org/en/austria/#requesting-districts) |
| [List Austrian Federal Provinces](actions/list-austrian-federal-provinces.md) | `GET /at/FederalProvinces` | [docs](https://www.openplzapi.org/en/austria/#requesting-federal-provinces) |
| [List Austrian Municipalities by Federal Province](actions/list-austrian-municipalities-by-federal-province.md) | `GET /at/FederalProvinces/{key}/Municipalities` | [docs](https://www.openplzapi.org/en/austria/#requesting-municipalities) |
| [List German Districts by Federal State](actions/list-german-districts-by-federal-state.md) | `GET /de/FederalStates/{key}/Districts` | [docs](https://www.openplzapi.org/en/germany/#requesting-districts) |
| [List German Federal States](actions/list-german-federal-states.md) | `GET /de/FederalStates` | [docs](https://www.openplzapi.org/en/germany/#requesting-federal-states) |
| [List German Government Regions by Federal State](actions/list-german-government-regions-by-federal-state.md) | `GET /de/FederalStates/{key}/GovernmentRegions` | [docs](https://www.openplzapi.org/en/germany/#requesting-government-regions) |
| [List German Municipalities by Federal State](actions/list-german-municipalities-by-federal-state.md) | `GET /de/FederalStates/{key}/Municipalities` | [docs](https://www.openplzapi.org/en/germany/#requesting-municipalities) |
| [List Liechtenstein Communes](actions/list-liechtenstein-communes.md) | `GET /li/Communes` | [docs](https://www.openplzapi.org/en/liechtenstein/#requesting-communes) |
| [List Swiss Cantons](actions/list-swiss-cantons.md) | `GET /ch/Cantons` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-cantons) |
| [List Swiss Communes by Canton](actions/list-swiss-communes-by-canton.md) | `GET /ch/Cantons/{key}/Communes` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-communes) |
| [List Swiss Districts by Canton](actions/list-swiss-districts-by-canton.md) | `GET /ch/Cantons/{key}/Districts` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-districts) |
| [List Swiss Localities by Canton](actions/list-swiss-localities-by-canton.md) | `GET /ch/Cantons/{key}/Localities` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-postal-codes-and-localities) |
| [Search Austrian Localities](actions/search-austrian-localities.md) | `GET /at/Localities` | [docs](https://www.openplzapi.org/en/austria/#requesting-postal-codes-and-localities) |
| [Search Austrian Streets](actions/search-austrian-streets.md) | `GET /at/Streets` | [docs](https://www.openplzapi.org/en/austria/#requesting-streets) |
| [Search German Localities](actions/search-german-localities.md) | `GET /de/Localities` | [docs](https://www.openplzapi.org/en/germany/#requesting-postal-codes-and-localities) |
| [Search German Streets](actions/search-german-streets.md) | `GET /de/Streets` | [docs](https://www.openplzapi.org/en/germany/#requesting-streets) |
| [Search Liechtenstein Localities](actions/search-liechtenstein-localities.md) | `GET /li/Localities` | [docs](https://www.openplzapi.org/en/liechtenstein/#requesting-postal-codes-and-localities) |
| [Search Liechtenstein Streets](actions/search-liechtenstein-streets.md) | `GET /li/Streets` | [docs](https://www.openplzapi.org/en/liechtenstein/#requesting-streets) |
| [Search Swiss Localities](actions/search-swiss-localities.md) | `GET /ch/Localities` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-postal-codes-and-localities) |
| [Search Swiss Streets](actions/search-swiss-streets.md) | `GET /ch/Streets` | [docs](https://www.openplzapi.org/en/switzerland/#requesting-streets) |
