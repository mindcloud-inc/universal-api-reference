# Calculoid: Native API Reference

A consolidated summary of Calculoid's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.calculoid.com/documentation-new
- **API base URL:** `https://api.calculoid.com`

## Authentication

### API Key

Authenticate Calculoid API requests with the profile ApiKeyHeader value sent as X-Calculoid-Api-Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Calculoid-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.calculoid.com/documentation-new)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Calculator](actions/copy-calculator.md) | `GET /calculator/copy/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [Create Field Option](actions/create-field-option.md) | `POST /option/create` | [docs](https://www.calculoid.com/documentation-new) |
| [Create Table](actions/create-table.md) | `POST /calculator/:calculatorId/tables/create` | [docs](https://www.calculoid.com/documentation-new) |
| [Delete Calculator](actions/delete-calculator.md) | `POST /calculator/delete/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [Delete Field](actions/delete-field.md) | `POST /calculator/deleteField/:fieldId` | [docs](https://www.calculoid.com/documentation-new) |
| [Delete Field Option](actions/delete-field-option.md) | `POST /option/delete/:optionId` | [docs](https://www.calculoid.com/documentation-new) |
| [Delete Submission](actions/delete-submission.md) | `POST /submission/delete/:submissionId` | [docs](https://www.calculoid.com/documentation-new) |
| [Delete Table](actions/delete-table.md) | `POST /calculator/:calculatorId/tables/:tableId/delete` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Calculator](actions/get-calculator.md) | `GET /calculator/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Calculator Report](actions/get-calculator-report.md) | `GET /calculator/report/:calculatorId/:tab` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Geo IP](actions/get-geo-ip.md) | `GET /geoIP/` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Result](actions/get-result.md) | `GET /result/:resultId` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Submission](actions/get-submission.md) | `GET /submission/:submissionId` | [docs](https://www.calculoid.com/documentation-new) |
| [Get Table](actions/get-table.md) | `GET /calculator/:calculatorId/tables/:tableId` | [docs](https://www.calculoid.com/documentation-new) |
| [Import Calculator](actions/import-calculator.md) | `POST /calculators/import` | [docs](https://www.calculoid.com/documentation-new) |
| [List Calculator Results](actions/list-calculator-results.md) | `GET /results/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [List Calculator Templates](actions/list-calculator-templates.md) | `GET /calculators/templates` | [docs](https://www.calculoid.com/documentation-new) |
| [List Calculator Webhooks](actions/list-calculator-webhooks.md) | `GET /calculator/:calculatorId/webhooks` | [docs](https://www.calculoid.com/documentation-new) |
| [List Calculators](actions/list-calculators.md) | `GET /calculators/` | [docs](https://www.calculoid.com/documentation-new) |
| [List Languages](actions/list-languages.md) | `GET /languages/` | [docs](https://www.calculoid.com/documentation-new) |
| [List Statistic Domains](actions/list-statistic-domains.md) | `GET /statistic/domains` | [docs](https://www.calculoid.com/documentation-new) |
| [List Submissions](actions/list-submissions.md) | `GET /submissions/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [List Tables](actions/list-tables.md) | `GET /calculator/:calculatorId/tables` | [docs](https://www.calculoid.com/documentation-new) |
| [List Tags](actions/list-tags.md) | `GET /tags/:limit/:search` | [docs](https://www.calculoid.com/documentation-new) |
| [Rate Calculator](actions/rate-calculator.md) | `POST /calculator/rate/:calculatorId` | [docs](https://www.calculoid.com/documentation-new) |
| [Update Table](actions/update-table.md) | `POST /calculator/:calculatorId/tables/:tableId/edit` | [docs](https://www.calculoid.com/documentation-new) |
