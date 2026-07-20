# ProfitWell: Native API Reference

A consolidated summary of ProfitWell's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://classic.paddle.com/profitwell/
- **OpenAPI specification:** https://classic.paddle.com/api-specifications/profitwell-v2.yaml
- **API base URL:** `https://api.profitwell.com`

## Authentication

### Private API Token

Use a ProfitWell private API token from Account Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.paddle.com/help/profitwell-metrics/setup/get-started/profit-well-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 250; maximum 250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Anonymize Customer By Email](actions/anonymize-customer-by-email.md) | `POST /v2/gdpr/anonymize_by_email/:email/` | [docs](https://classic.paddle.com/profitwell/) |
| [Anonymize Customer By ID](actions/anonymize-customer-by-id.md) | `POST /v2/gdpr/anonymize_by_customer_id/:customer_id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Churn Subscription](actions/churn-subscription.md) | `DELETE /v2/subscriptions/:subscriptionIdOrSubscriptionAlias/` | [docs](https://classic.paddle.com/profitwell/) |
| [Create Customer Event](actions/create-customer-event.md) | `POST https://api.profitwell-events.com/dotjs/v1/customer/event` | [docs](https://classic.paddle.com/profitwell/) |
| [Create Or Update Customer Trait](actions/create-or-update-customer-trait.md) | `PUT /v2/customer_traits/trait/` | [docs](https://classic.paddle.com/profitwell/) |
| [Create Plan](actions/create-plan.md) | `POST /v2/plans/` | [docs](https://classic.paddle.com/profitwell/) |
| [Create Subscription](actions/create-subscription.md) | `POST /v2/subscriptions/` | [docs](https://classic.paddle.com/profitwell/) |
| [Delete User](actions/delete-user.md) | `DELETE /v2/users/:userIdOrUserAlias/` | [docs](https://classic.paddle.com/profitwell/) |
| [Exclude Customer From Metrics](actions/exclude-customer-from-metrics.md) | `POST /v2/metrics/exclude_customer/:customer_id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Get API Status](actions/get-api-status.md) | `GET /v2/api-status` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /v2/company/settings` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Customer Traits](actions/get-customer-traits.md) | `GET /v2/customer_traits/customer/:customer_id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Daily Metrics](actions/get-daily-metrics.md) | `GET /v2/metrics/daily` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Monthly Metrics](actions/get-monthly-metrics.md) | `GET /v2/metrics/monthly` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Plan IDs](actions/get-plan-ids.md) | `GET /v2/metrics/plans` | [docs](https://classic.paddle.com/profitwell/) |
| [Get Subscription History For User](actions/get-subscription-history-for-user.md) | `GET /v2/users/:userIdOrUserAlias/` | [docs](https://classic.paddle.com/profitwell/) |
| [List Manually-Added Plans](actions/list-manually-added-plans.md) | `GET /v2/plans/` | [docs](https://classic.paddle.com/profitwell/) |
| [List Retain Unsubscribed Customers](actions/list-retain-unsubscribed-customers.md) | `GET /v2/retain/unsubscribed_customers/:intervention_type/` | [docs](https://classic.paddle.com/profitwell/) |
| [Remove Customer Trait](actions/remove-customer-trait.md) | `DELETE /v2/customer_traits/trait/` | [docs](https://classic.paddle.com/profitwell/) |
| [Remove Trait Category](actions/remove-trait-category.md) | `DELETE /v2/customer_traits/category/` | [docs](https://classic.paddle.com/profitwell/) |
| [Retrieve Customer By ID](actions/retrieve-customer-by-id.md) | `GET /v2/customers/:customer_id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Retrieve Plan](actions/retrieve-plan.md) | `GET /v2/plans/:id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Search Customers](actions/search-customers.md) | `GET /v2/customers/` | [docs](https://classic.paddle.com/profitwell/) |
| [Stop Retain For Customer](actions/stop-retain-for-customer.md) | `POST /v2/retain/stop/` | [docs](https://classic.paddle.com/profitwell/) |
| [Un-Churn Subscription](actions/un-churn-subscription.md) | `PUT /v2/unchurn/:subscriptionIdOrSubscriptionAlias/` | [docs](https://classic.paddle.com/profitwell/) |
| [Update Plan](actions/update-plan.md) | `PUT /v2/plans/:id/` | [docs](https://classic.paddle.com/profitwell/) |
| [Update User](actions/update-user.md) | `PUT /v2/users/:userIdOrUserAlias/` | [docs](https://classic.paddle.com/profitwell/) |
| [Upgrade Or Downgrade Subscription](actions/upgrade-or-downgrade-subscription.md) | `PUT /v2/subscriptions/:subscriptionIdOrSubscriptionAlias/` | [docs](https://classic.paddle.com/profitwell/) |
