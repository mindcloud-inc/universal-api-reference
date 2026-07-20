# condoo: Native API Reference

A consolidated summary of condoo's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://trk.condoo.systems/en/api-documentation
- **API base URL:** `https://trk.condoo.systems/api`

## Authentication

### API Key

Bearer API key authentication for Condoo Analytics.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://trk.condoo.systems/en/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `results_per_page` in the query string to set the page size (default 25; accepted range 10–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_type`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Domain](actions/create-custom-domain.md) | `POST /domains` | [docs](https://trk.condoo.systems/en/api-documentation/domains) |
| [Create Goal](actions/create-goal.md) | `POST /goals` | [docs](https://trk.condoo.systems/en/api-documentation/goals) |
| [Create Goal Conversion](actions/create-goal-conversion.md) | `POST /goals-conversions` | [docs](https://trk.condoo.systems/en/api-documentation/goals-conversions) |
| [Create Pageview](actions/create-pageview.md) | `POST /pageviews-lightweight` | [docs](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight) |
| [Create Website](actions/create-website.md) | `POST /websites` | [docs](https://trk.condoo.systems/en/api-documentation/websites) |
| [Delete Custom Domain](actions/delete-custom-domain.md) | `DELETE /domains/{domain_id}` | [docs](https://trk.condoo.systems/en/api-documentation/domains) |
| [Delete Goal](actions/delete-goal.md) | `DELETE /goals/{goal_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals) |
| [Delete Goal Conversion](actions/delete-goal-conversion.md) | `DELETE /goals-conversions/{conversion_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals-conversions) |
| [Delete Pageview](actions/delete-pageview.md) | `DELETE /pageviews-lightweight/{event_id}` | [docs](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight) |
| [Delete Visitor](actions/delete-visitor.md) | `DELETE /visitors/{visitor_id}` | [docs](https://trk.condoo.systems/en/api-documentation/visitors) |
| [Delete Website](actions/delete-website.md) | `DELETE /websites/{website_id}` | [docs](https://trk.condoo.systems/en/api-documentation/websites) |
| [List Account Logs](actions/list-account-logs.md) | `GET /logs/` | [docs](https://trk.condoo.systems/en/api-documentation/users-logs) |
| [List Account Payments](actions/list-account-payments.md) | `GET /payments/` | [docs](https://trk.condoo.systems/en/api-documentation/payments) |
| [List Custom Domains](actions/list-custom-domains.md) | `GET /domains/` | [docs](https://trk.condoo.systems/en/api-documentation/domains) |
| [List Goal Conversions](actions/list-goal-conversions.md) | `GET /goals-conversions/` | [docs](https://trk.condoo.systems/en/api-documentation/goals-conversions) |
| [List Goals](actions/list-goals.md) | `GET /goals/` | [docs](https://trk.condoo.systems/en/api-documentation/goals) |
| [List Pageviews](actions/list-pageviews.md) | `GET /pageviews-lightweight/` | [docs](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight) |
| [List Visitors](actions/list-visitors.md) | `GET /visitors/` | [docs](https://trk.condoo.systems/en/api-documentation/visitors) |
| [List Websites](actions/list-websites.md) | `GET /websites/` | [docs](https://trk.condoo.systems/en/api-documentation/websites) |
| [Retrieve Account Payment](actions/retrieve-account-payment.md) | `GET /payments/{payment_id}` | [docs](https://trk.condoo.systems/en/api-documentation/payments) |
| [Retrieve Custom Domain](actions/retrieve-custom-domain.md) | `GET /domains/{domain_id}` | [docs](https://trk.condoo.systems/en/api-documentation/domains) |
| [Retrieve Goal](actions/retrieve-goal.md) | `GET /goals/{goal_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals) |
| [Retrieve Goal Conversion](actions/retrieve-goal-conversion.md) | `GET /goals-conversions/{conversion_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals-conversions) |
| [Retrieve Pageview](actions/retrieve-pageview.md) | `GET /pageviews-lightweight/{event_id}` | [docs](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight) |
| [Retrieve User](actions/retrieve-user.md) | `GET /user` | [docs](https://trk.condoo.systems/en/api-documentation/user) |
| [Retrieve Visitor](actions/retrieve-visitor.md) | `GET /visitors/{visitor_id}` | [docs](https://trk.condoo.systems/en/api-documentation/visitors) |
| [Retrieve Website](actions/retrieve-website.md) | `GET /websites/{website_id}` | [docs](https://trk.condoo.systems/en/api-documentation/websites) |
| [Retrieve Website Statistics](actions/retrieve-website-statistics.md) | `GET /statistics/{website_id}` | [docs](https://trk.condoo.systems/en/api-documentation/statistics) |
| [Update Custom Domain](actions/update-custom-domain.md) | `POST /domains/{domain_id}` | [docs](https://trk.condoo.systems/en/api-documentation/domains) |
| [Update Goal](actions/update-goal.md) | `POST /goals/{goal_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals) |
| [Update Goal Conversion](actions/update-goal-conversion.md) | `POST /goals-conversions/{conversion_id}` | [docs](https://trk.condoo.systems/en/api-documentation/goals-conversions) |
| [Update Pageview](actions/update-pageview.md) | `POST /pageviews-lightweight/{event_id}` | [docs](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight) |
| [Update Visitor](actions/update-visitor.md) | `POST /visitors/{visitor_id}` | [docs](https://trk.condoo.systems/en/api-documentation/visitors) |
| [Update Website](actions/update-website.md) | `POST /websites/{website_id}` | [docs](https://trk.condoo.systems/en/api-documentation/websites) |
