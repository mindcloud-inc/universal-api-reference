# CallRail: Native API Reference

A consolidated summary of CallRail's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.callrail.com/
- **API base URL:** `https://api.callrail.com`

## Authentication

### API Key

Authenticate with a personal or user-scoped CallRail API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Token token="<apiKey>"
```

[Official authentication documentation](https://apidocs.callrail.com/#authorization)

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /v3/a/:account_id/companies.json` | [docs](https://apidocs.callrail.com/#creating-a-company) |
| [Create Form Submission](actions/create-form-submission.md) | `POST /v3/a/:account_id/form_submissions.json` | [docs](https://apidocs.callrail.com/#creating-a-form-submission) |
| [Create Tag](actions/create-tag.md) | `POST /v3/a/:account_id/tags.json` | [docs](https://apidocs.callrail.com/#creating-a-tag) |
| [Disable Company](actions/disable-company.md) | `DELETE /v3/a/:account_id/companies/:company_id.json` | [docs](https://apidocs.callrail.com/#disabling-a-company) |
| [Get Account](actions/get-account.md) | `GET /v3/a/:account_id.json` | [docs](https://apidocs.callrail.com/#retrieving-a-single-account) |
| [Get Call](actions/get-call.md) | `GET /v3/a/:account_id/calls/:call_id.json` | [docs](https://apidocs.callrail.com/#retrieving-a-single-call) |
| [Get Call Recording](actions/get-call-recording.md) | `GET /v3/a/:account_id/calls/:call_id/recording.json` | [docs](https://apidocs.callrail.com/#retrieving-a-single-call-recording) |
| [Get Company](actions/get-company.md) | `GET /v3/a/:account_id/companies/:company_id.json` | [docs](https://apidocs.callrail.com/#retrieving-a-single-company) |
| [List Accounts](actions/list-accounts.md) | `GET /v3/a.json` | [docs](https://apidocs.callrail.com/#listing-all-accounts) |
| [List Call Page Views](actions/list-call-page-views.md) | `GET /v3/a/:account_id/calls/:call_id/page_views.json` | [docs](https://apidocs.callrail.com/#retrieving-all-page-views-for-a-call) |
| [List Calls](actions/list-calls.md) | `GET /v3/a/:account_id/calls.json` | [docs](https://apidocs.callrail.com/#listing-all-calls) |
| [List Companies](actions/list-companies.md) | `GET /v3/a/:account_id/companies.json` | [docs](https://apidocs.callrail.com/#listing-all-companies) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /v3/a/:account_id/form_submissions.json` | [docs](https://apidocs.callrail.com/#listing-all-form-submissions) |
| [List Tags](actions/list-tags.md) | `GET /v3/a/:account_id/tags.json` | [docs](https://apidocs.callrail.com/#retrieving-all-tags) |
| [Remove Tag](actions/remove-tag.md) | `DELETE /v3/a/:account_id/tags/:tag_id.json` | [docs](https://apidocs.callrail.com/#removing-a-tag) |
| [Summarize Call Data](actions/summarize-call-data.md) | `GET /v3/a/:account_id/calls/summary.json` | [docs](https://apidocs.callrail.com/#summarizing-call-data) |
| [Summarize Call Data By Time Series](actions/summarize-call-data-by-time-series.md) | `GET /v3/a/:account_id/calls/timeseries.json` | [docs](https://apidocs.callrail.com/#summarizing-call-data-by-time-series) |
| [Summarize Form Data](actions/summarize-form-data.md) | `GET /v3/a/:account_id/forms/summary.json` | [docs](https://apidocs.callrail.com/#summarizing-form-data) |
| [Update Call](actions/update-call.md) | `PUT /v3/a/:account_id/calls/:call_id.json` | [docs](https://apidocs.callrail.com/#updating-a-call) |
| [Update Company](actions/update-company.md) | `PUT /v3/a/:account_id/companies/:company_id.json` | [docs](https://apidocs.callrail.com/#updating-a-company) |
| [Update Form Submission](actions/update-form-submission.md) | `PUT /v3/a/:account_id/form_submissions/:form_submission_id.json` | [docs](https://apidocs.callrail.com/#updating-a-form-submission) |
| [Update Tag](actions/update-tag.md) | `PUT /v3/a/:account_id/tags/:tag_id.json` | [docs](https://apidocs.callrail.com/#updating-a-tag) |
