# openFDA Drug: Native API Reference

A consolidated summary of openFDA Drug's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://open.fda.gov/apis/drug/
- **API base URL:** `https://api.fda.gov`

## Authentication

### No Authentication

The selected openFDA Drug endpoints are public HTTPS JSON endpoints and can be called without tenant credentials. Optional API keys only increase quota and are not required for this app build.

This API does not require request authentication.

[Official authentication documentation](https://open.fda.gov/apis/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud openFDA Drug App/1.0` |

Responses from this API use JSON.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md) | `GET /drug/event.json` | [docs](https://open.fda.gov/apis/drug/event/how-to-use-the-endpoint/) |
| [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md) | `GET /drug/enforcement.json` | [docs](https://open.fda.gov/apis/drug/enforcement/how-to-use-the-endpoint/) |
| [Count Drug Label Records](actions/count-drug-label-records.md) | `GET /drug/label.json` | [docs](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/) |
| [Count Drug NDC Records](actions/count-drug-ndc-records.md) | `GET /drug/ndc.json` | [docs](https://open.fda.gov/apis/drug/ndc/how-to-use-the-endpoint/) |
| [Count Drug Shortage Records](actions/count-drug-shortage-records.md) | `GET /drug/shortages.json` | [docs](https://open.fda.gov/apis/drug/drugshortages/how-to-use-the-endpoint/) |
| [Count Drugs@FDA Records](actions/count-drugs-fda-records.md) | `GET /drug/drugsfda.json` | [docs](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/) |
| [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md) | `GET /drug/event.json` | [docs](https://open.fda.gov/apis/drug/event/how-to-use-the-endpoint/) |
| [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md) | `GET /drug/enforcement.json` | [docs](https://open.fda.gov/apis/drug/enforcement/how-to-use-the-endpoint/) |
| [Search Drug Label Records](actions/search-drug-label-records.md) | `GET /drug/label.json` | [docs](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/) |
| [Search Drug NDC Records](actions/search-drug-ndc-records.md) | `GET /drug/ndc.json` | [docs](https://open.fda.gov/apis/drug/ndc/how-to-use-the-endpoint/) |
| [Search Drug Shortage Records](actions/search-drug-shortage-records.md) | `GET /drug/shortages.json` | [docs](https://open.fda.gov/apis/drug/drugshortages/how-to-use-the-endpoint/) |
| [Search Drugs@FDA Records](actions/search-drugs-fda-records.md) | `GET /drug/drugsfda.json` | [docs](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/) |
