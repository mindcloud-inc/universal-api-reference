# Cursion: Native API Reference

A consolidated summary of Cursion's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.cursion.dev
- **API base URL:** `https://api.cursion.dev/v1/ops`

## Authentication

### API Token

Use a Cursion API token. The provider expects Authorization: Token <api_token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cursion.dev/api/site)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Alert](actions/create-alert.md) | `POST /alert` | [docs](https://docs.cursion.dev/api/alert) |
| [Create Issue](actions/create-issue.md) | `POST /issue` | [docs](https://docs.cursion.dev/api/issue) |
| [Create Page](actions/create-page.md) | `POST /page` | [docs](https://docs.cursion.dev/api/page) |
| [Create Report](actions/create-report.md) | `POST /report` | [docs](https://docs.cursion.dev/api/report) |
| [Create Scan](actions/create-scan.md) | `POST /scan` | [docs](https://docs.cursion.dev/api/scan) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedule` | [docs](https://docs.cursion.dev/api/schedule) |
| [Create Site](actions/create-site.md) | `POST /site` | [docs](https://docs.cursion.dev/api/site) |
| [Create Test](actions/create-test.md) | `POST /test` | [docs](https://docs.cursion.dev/api/test) |
| [Delete Alert](actions/delete-alert.md) | `DELETE /alert/{{alertId}}` | [docs](https://docs.cursion.dev/api/alert) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /issue/{{issueId}}` | [docs](https://docs.cursion.dev/api/issue) |
| [Delete Page](actions/delete-page.md) | `DELETE /page/{{pageId}}` | [docs](https://docs.cursion.dev/api/page) |
| [Delete Pages](actions/delete-pages.md) | `POST /pages/delete` | [docs](https://docs.cursion.dev/api/page) |
| [Delete Report](actions/delete-report.md) | `DELETE /report/{{reportId}}` | [docs](https://docs.cursion.dev/api/report) |
| [Delete Scan](actions/delete-scan.md) | `DELETE /scan/{{scanId}}` | [docs](https://docs.cursion.dev/api/scan) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedule/{{scheduleId}}` | [docs](https://docs.cursion.dev/api/schedule) |
| [Delete Site](actions/delete-site.md) | `DELETE /site/{{siteId}}` | [docs](https://docs.cursion.dev/api/site) |
| [Delete Sites](actions/delete-sites.md) | `POST /sites/delete` | [docs](https://docs.cursion.dev/api/site) |
| [Delete Test](actions/delete-test.md) | `DELETE /test/{{testId}}` | [docs](https://docs.cursion.dev/api/test) |
| [Generate Issue](actions/generate-issue.md) | `POST /issue/generate` | [docs](https://docs.cursion.dev/api/issue) |
| [Get Alert](actions/get-alert.md) | `GET /alert/{{alertId}}` | [docs](https://docs.cursion.dev/api/alert) |
| [Get Issue](actions/get-issue.md) | `GET /issue/{{issueId}}` | [docs](https://docs.cursion.dev/api/issue) |
| [Get Lean Scan](actions/get-lean-scan.md) | `GET /scan/{{scanId}}/lean` | [docs](https://docs.cursion.dev/api/scan) |
| [Get Lean Test](actions/get-lean-test.md) | `GET /test/{{testId}}/lean` | [docs](https://docs.cursion.dev/api/test) |
| [Get Page](actions/get-page.md) | `GET /page/{{pageId}}` | [docs](https://docs.cursion.dev/api/page) |
| [Get Report](actions/get-report.md) | `GET /report/{{reportId}}` | [docs](https://docs.cursion.dev/api/report) |
| [Get Scan](actions/get-scan.md) | `GET /scan/{{scanId}}` | [docs](https://docs.cursion.dev/api/scan) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedule/{{scheduleId}}` | [docs](https://docs.cursion.dev/api/schedule) |
| [Get Site](actions/get-site.md) | `GET /site/{{siteId}}` | [docs](https://docs.cursion.dev/api/site) |
| [Get Test](actions/get-test.md) | `GET /test/{{testId}}` | [docs](https://docs.cursion.dev/api/test) |
| [List Alerts](actions/list-alerts.md) | `GET /alert` | [docs](https://docs.cursion.dev/api/alert) |
| [List Issues](actions/list-issues.md) | `GET /issue` | [docs](https://docs.cursion.dev/api/issue) |
| [List Pages](actions/list-pages.md) | `GET /page` | [docs](https://docs.cursion.dev/api/page) |
| [List Reports](actions/list-reports.md) | `GET /report` | [docs](https://docs.cursion.dev/api/report) |
| [List Scans](actions/list-scans.md) | `GET /scan` | [docs](https://docs.cursion.dev/api/scan) |
| [List Schedules](actions/list-schedules.md) | `GET /schedule` | [docs](https://docs.cursion.dev/api/schedule) |
| [List Sites](actions/list-sites.md) | `GET /site` | [docs](https://docs.cursion.dev/api/site) |
| [List Tests](actions/list-tests.md) | `GET /test` | [docs](https://docs.cursion.dev/api/test) |
