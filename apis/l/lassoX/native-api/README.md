# Lasso X: Native API Reference

A consolidated summary of Lasso X's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.lassox.com/
- **API base URL:** `https://api.lassox.com`

## Authentication

### API Key

Lasso X API key authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
lasso-api-key: <apiKey>
```

[Official authentication documentation](https://docs.lassox.com/gettingstarted/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Financial Report](actions/analyze-financial-report.md) | `POST /modules/reportanalysis/:lassoId` | [docs](https://docs.lassox.com/module-apis/financial-analysis/) |
| [Create Reporting Batch](actions/create-reporting-batch.md) | `POST /apps/reporting/batches` | [docs](https://docs.lassox.com/module-apis/reporting/#schedule-a-report) |
| [Download Latest Report PDF](actions/download-latest-report-pdf.md) | `GET /:lassoId/reports/latest/pdf` | [docs](https://docs.lassox.com/data-apis/cvr/#reports) |
| [Get CreditSafe Rating](actions/get-creditsafe-rating.md) | `GET /data/creditsafe/rating/:cvr` | [docs](https://docs.lassox.com/data-apis/creditsafe/) |
| [Get CVR Entity](actions/get-cvr-entity.md) | `GET /:lassoId` | [docs](https://docs.lassox.com/data-apis/cvr/#basic-info-staminformation) |
| [Get CVR Entity History](actions/get-cvr-entity-history.md) | `GET /:lassoId/history` | [docs](https://docs.lassox.com/data-apis/cvr/#basic-info-staminformation) |
| [Get Latest Report](actions/get-latest-report.md) | `GET /:lassoId/reports/latest` | [docs](https://docs.lassox.com/data-apis/cvr/#reports) |
| [Get Network](actions/get-network.md) | `GET /modules/network/:lassoId` | [docs](https://docs.lassox.com/module-apis/cvrnetwork/) |
| [Get Paqle Entity](actions/get-paqle-entity.md) | `GET /data/paqle/:lassoId/entity` | [docs](https://docs.lassox.com/data-apis/paqle/) |
| [Get Property Summary](actions/get-property-summary.md) | `GET /data/bbr/property/summary` | [docs](https://docs.lassox.com/data-apis/bbr/) |
| [Get Related People](actions/get-related-people.md) | `GET /:lassoId/related/person` | [docs](https://docs.lassox.com/data-apis/cvr/#related-data) |
| [Get Related People History](actions/get-related-people-history.md) | `GET /:lassoId/related/person/history` | [docs](https://docs.lassox.com/data-apis/cvr/#related-data) |
| [Get Reporting Batch](actions/get-reporting-batch.md) | `GET /apps/reporting/batches/:id` | [docs](https://docs.lassox.com/module-apis/reporting/#retrieve-reports) |
| [List Company Delta](actions/list-company-delta.md) | `GET /data/cvr/company/delta` | [docs](https://docs.lassox.com/data-apis/cvr/#getting-changes-delta) |
| [List Paqle News](actions/list-paqle-news.md) | `GET /data/paqle/:lassoId/news` | [docs](https://docs.lassox.com/data-apis/paqle/) |
| [List Person Delta](actions/list-person-delta.md) | `GET /data/cvr/person/delta` | [docs](https://docs.lassox.com/data-apis/cvr/#getting-changes-delta) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /data/teledata/:lassoId/phonenumbers` | [docs](https://docs.lassox.com/data-apis/teledata/) |
| [List Production Unit Delta](actions/list-production-unit-delta.md) | `GET /data/cvr/place/delta` | [docs](https://docs.lassox.com/data-apis/cvr/#getting-changes-delta) |
| [List Report Delta](actions/list-report-delta.md) | `GET /data/cvr/reports/delta` | [docs](https://docs.lassox.com/data-apis/cvr/#reports) |
| [List Reporting Batch Items](actions/list-reporting-batch-items.md) | `GET /apps/reporting/batches/:id/items` | [docs](https://docs.lassox.com/module-apis/reporting/#retrieve-reports) |
| [List Reporting Batches](actions/list-reporting-batches.md) | `GET /apps/reporting/batches` | [docs](https://docs.lassox.com/module-apis/reporting/#retrieve-reports) |
| [List Reports](actions/list-reports.md) | `GET /:lassoId/reports` | [docs](https://docs.lassox.com/data-apis/cvr/#reports) |
| [Lookup Phone Number](actions/lookup-phone-number.md) | `GET /data/teledata/:phoneNumber` | [docs](https://docs.lassox.com/data-apis/teledata/) |
| [Search CVR](actions/search-cvr.md) | `GET /data/cvr/search` | [docs](https://docs.lassox.com/data-apis/cvr/#search) |
