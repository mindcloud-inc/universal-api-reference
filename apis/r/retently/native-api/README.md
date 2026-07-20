# Retently: Native API Reference

A consolidated summary of Retently's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.retently.com/api/
- **API base URL:** `https://app.retently.com`

## Authentication

### API Key

Connect Retently with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.retently.com/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.pages`. The current page number is read from `data.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Feedback Tags](actions/add-feedback-tags.md) | `POST /api/v2/response/tags` | [docs](https://www.retently.com/api/#api-add-response-tags-post) |
| [Add Feedback Topics](actions/add-feedback-topics.md) | `POST /api/v2/response/topics` | [docs](https://www.retently.com/api/#api-add-response-topics-post) |
| [Add Suppressed Domain](actions/add-suppressed-domain.md) | `POST /api/v2/suppressions/domains` | [docs](https://www.retently.com/api/#api-post-suppressions-domains) |
| [Add Suppressed Email](actions/add-suppressed-email.md) | `POST /api/v2/suppressions/emails` | [docs](https://www.retently.com/api/#api-post-suppressions-emails) |
| [Delete Customers](actions/delete-customers.md) | `DELETE /api/v2/customers` | [docs](https://www.retently.com/api/#api-delete-customers-delete) |
| [Get Company](actions/get-company.md) | `GET /api/v2/companies/:companyIdOrDomain` | [docs](https://www.retently.com/api/#api-get-company-by-id-get) |
| [Get Customer](actions/get-customer.md) | `GET /api/v2/customers/:customerId` | [docs](https://www.retently.com/api/#api-get-customer-get-by-id) |
| [Get Feedback](actions/get-feedback.md) | `GET /api/v2/feedback/:feedbackId` | [docs](https://www.retently.com/api/#api-get-feedback-get-by-id) |
| [Get Group Trends](actions/get-group-trends.md) | `GET /api/v2/trends/:groupId` | [docs](https://www.retently.com/api/#api-get-trends-group-get) |
| [Get Latest Score](actions/get-latest-score.md) | `GET /api/v2/:metric/score` | [docs](https://www.retently.com/api/#api-get-latest-score-get) |
| [List Campaign Reports](actions/list-campaign-reports.md) | `GET /api/v2/reports` | [docs](https://www.retently.com/api/#api-get-reports-get) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v2/campaigns` | [docs](https://www.retently.com/api/#api-get-campaigns-get) |
| [List Companies](actions/list-companies.md) | `GET /api/v2/companies` | [docs](https://www.retently.com/api/#api-get-companies-get) |
| [List Customers](actions/list-customers.md) | `GET /api/v2/customers` | [docs](https://www.retently.com/api/#api-get-customers-get) |
| [List Feedback](actions/list-feedback.md) | `GET /api/v2/feedback` | [docs](https://www.retently.com/api/#api-get-feedback-get) |
| [List Outbox](actions/list-outbox.md) | `GET /api/v2/outbox` | [docs](https://www.retently.com/api/#api-get-sent-surveys) |
| [List Suppressed Domains](actions/list-suppressed-domains.md) | `GET /api/v2/suppressions/domains` | [docs](https://www.retently.com/api/#api-get-suppressions-domains) |
| [List Suppressed Emails](actions/list-suppressed-emails.md) | `GET /api/v2/suppressions/emails` | [docs](https://www.retently.com/api/#api-get-suppressions-emails) |
| [List Templates](actions/list-templates.md) | `GET /api/v2/templates` | [docs](https://www.retently.com/api/#api-get-templates-get) |
| [List Trend Groups](actions/list-trend-groups.md) | `GET /api/v2/trends` | [docs](https://www.retently.com/api/#api-get-trends-get) |
| [Remove Suppressed Domain](actions/remove-suppressed-domain.md) | `DELETE /api/v2/suppressions/domains/:id` | [docs](https://www.retently.com/api/#api-delete-suppressions-domain) |
| [Remove Suppressed Email](actions/remove-suppressed-email.md) | `DELETE /api/v2/suppressions/emails/:id` | [docs](https://www.retently.com/api/#api-delete-suppressions-email) |
| [Send Transactional Survey](actions/send-transactional-survey.md) | `POST /api/v2/survey` | [docs](https://www.retently.com/api/#api-send-transactional-survey) |
| [Unsubscribe Customers](actions/unsubscribe-customers.md) | `POST /api/v2/customers/unsubscribe` | [docs](https://www.retently.com/api/#api-unsubscribe-customers-post) |
| [Upsert Customers](actions/upsert-customers.md) | `POST /api/v2/customers` | [docs](https://www.retently.com/api/#api-create-or-update-customers-post) |
