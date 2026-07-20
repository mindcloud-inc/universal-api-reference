# QADeputy: Native API Reference

A consolidated summary of QADeputy's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.qadeputy.com/
- **API base URL:** `https://app.qadeputy.com/api/v1`

## Authentication

### API Key

Authenticate with a QADeputy API key in the Authorization header and a companion account email header.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required · Email address for an active QADeputy user in the account. MindCloud sends it in the required email header.

Send these headers with each API request:

```http
email: <email>
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.qadeputy.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort_field` in the query string. Set the direction separately with `sort_type`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Test Result](actions/create-test-result.md) | `POST /test-cases/:testCaseId/test-results` | [docs](https://apidocs.qadeputy.com/) |
| [Create Test Run](actions/create-test-run.md) | `POST /test-runs` | [docs](https://apidocs.qadeputy.com/) |
| [Create Test Suite](actions/create-test-suite.md) | `POST /test-suites` | [docs](https://apidocs.qadeputy.com/) |
| [Create Test Suite Test Case](actions/create-test-suite-test-case.md) | `POST /test-suites/:testSuiteId/test-cases` | [docs](https://apidocs.qadeputy.com/) |
| [Get Test Run](actions/get-test-run.md) | `GET /test-runs/:testRunId` | [docs](https://apidocs.qadeputy.com/) |
| [Get Test Suite](actions/get-test-suite.md) | `GET /test-suites/:testSuiteId` | [docs](https://apidocs.qadeputy.com/) |
| [Get Test Suite Test Case](actions/get-test-suite-test-case.md) | `GET /test-suites/:testSuiteId/test-cases/:testCaseId` | [docs](https://apidocs.qadeputy.com/) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Case Statuses](actions/list-test-case-statuses.md) | `GET /test-case-statuses` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Results](actions/list-test-results.md) | `GET /test-cases/:testCaseId/test-results` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Run Test Cases](actions/list-test-run-test-cases.md) | `GET /test-runs/:testRunId/test-cases` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Runs](actions/list-test-runs.md) | `GET /test-runs` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Suite Test Cases](actions/list-test-suite-test-cases.md) | `GET /test-suites/:testSuiteId/test-cases` | [docs](https://apidocs.qadeputy.com/) |
| [List Test Suites](actions/list-test-suites.md) | `GET /test-suites` | [docs](https://apidocs.qadeputy.com/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://apidocs.qadeputy.com/) |
| [Update Test Run](actions/update-test-run.md) | `PUT /test-runs/:testRunId` | [docs](https://apidocs.qadeputy.com/) |
| [Update Test Run Test Case](actions/update-test-run-test-case.md) | `PUT /test-runs/:testRunId/test-cases/:testCaseId` | [docs](https://apidocs.qadeputy.com/) |
| [Update Test Suite](actions/update-test-suite.md) | `PUT /test-suites/:testSuiteId` | [docs](https://apidocs.qadeputy.com/) |
| [Update Test Suite Test Case](actions/update-test-suite-test-case.md) | `PUT /test-suites/:testSuiteId/test-cases/:testCaseId` | [docs](https://apidocs.qadeputy.com/) |
