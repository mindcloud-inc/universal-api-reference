# PageVitals: Native API Reference

A consolidated summary of PageVitals's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://pagevitals.com/docs/rest-api/reference/
- **API base URL:** `https://api.pagevitals.com`

## Authentication

### API Key

Connect to PageVitals with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pagevitals.com/docs/rest-api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Settings Pages](actions/add-settings-pages.md) | `POST /:websiteId/settings/pages` | [docs](https://pagevitals.com/docs/rest-api/reference/settings/pages/) |
| [Add Website](actions/add-website.md) | `POST /account/websites` | [docs](https://pagevitals.com/docs/rest-api/reference/websites/) |
| [Create Budget](actions/create-budget.md) | `POST /:websiteId/budgets` | [docs](https://pagevitals.com/docs/rest-api/reference/budgets/) |
| [Create Multistep Test](actions/create-multistep-test.md) | `POST /:websiteId/multistep` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/list/) |
| [Get Multistep Test](actions/get-multistep-test.md) | `GET /:websiteId/multistep/:testId` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/detail/) |
| [Get Page](actions/get-page.md) | `GET /:websiteId/pages/:pageId` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/page-detail/) |
| [Get Page CrUX Timeline](actions/get-page-crux-timeline.md) | `GET /:websiteId/pages/:pageId/crux` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/crux/) |
| [Get Page Network Chart](actions/get-page-network-chart.md) | `GET /:websiteId/pages/:pageId/network` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/network/) |
| [Get Page Opportunity](actions/get-page-opportunity.md) | `GET /:websiteId/pages/:pageId/opportunities/:opportunityId` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/opportunities/) |
| [Get Page Timeline](actions/get-page-timeline.md) | `GET /:websiteId/pages/:pageId/timeline` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/timeline/) |
| [Get Test](actions/get-test.md) | `GET /:websiteId/tests/:testId` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-detail/) |
| [Get Test Waterfall](actions/get-test-waterfall.md) | `GET /:websiteId/tests/:testId/waterfall` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-detail/) |
| [List Budgets](actions/list-budgets.md) | `GET /:websiteId/budgets` | [docs](https://pagevitals.com/docs/rest-api/reference/budgets/) |
| [List Field Testing Resources](actions/list-field-testing-resources.md) | `GET /:websiteId/field-testing/resources` | [docs](https://pagevitals.com/docs/rest-api/reference/field-testing/resources/) |
| [List Multistep Test Runs](actions/list-multistep-test-runs.md) | `GET /:websiteId/multistep/:testId/runs` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/runs/) |
| [List Multistep Tests](actions/list-multistep-tests.md) | `GET /:websiteId/multistep` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/list/) |
| [List Page Opportunities](actions/list-page-opportunities.md) | `GET /:websiteId/pages/:pageId/opportunities` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/opportunities/) |
| [List Pages](actions/list-pages.md) | `GET /:websiteId/pages` | [docs](https://pagevitals.com/docs/rest-api/reference/pages/page-list/) |
| [List Settings Pages](actions/list-settings-pages.md) | `GET /:websiteId/settings/pages` | [docs](https://pagevitals.com/docs/rest-api/reference/settings/pages/) |
| [List Test Opportunities](actions/list-test-opportunities.md) | `GET /:websiteId/tests/:testId/opportunities` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-detail/) |
| [List Test Series](actions/list-test-series.md) | `GET /:websiteId/testseries` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-series/) |
| [List Tests in Test Series](actions/list-tests-in-test-series.md) | `GET /:websiteId/testseries/:seriesId` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-series/) |
| [List Website Opportunities](actions/list-website-opportunities.md) | `GET /:websiteId/opportunities` | [docs](https://pagevitals.com/docs/rest-api/reference/opportunities/) |
| [List Websites](actions/list-websites.md) | `GET /websites` | [docs](https://pagevitals.com/docs/rest-api/reference/websites/) |
| [Run All Multistep Tests](actions/run-all-multistep-tests.md) | `POST /:websiteId/multistep/run-all` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/list/) |
| [Run Multistep Test](actions/run-multistep-test.md) | `POST /:websiteId/multistep/:testId/runs` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/runs/) |
| [Run Tests](actions/run-tests.md) | `POST /:websiteId/testseries` | [docs](https://pagevitals.com/docs/rest-api/reference/tests/test-series/) |
| [Update Budget](actions/update-budget.md) | `PUT /:websiteId/budgets/:budgetId` | [docs](https://pagevitals.com/docs/rest-api/reference/budgets/) |
| [Update Multistep Test](actions/update-multistep-test.md) | `PUT /:websiteId/multistep/:testId` | [docs](https://pagevitals.com/docs/rest-api/reference/multistep/detail/) |
| [Update Settings Page](actions/update-settings-page.md) | `PUT /:websiteId/settings/pages/:pageId` | [docs](https://pagevitals.com/docs/rest-api/reference/settings/pages/) |
