# Tarvent: Native API Reference

A consolidated summary of Tarvent's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.tarvent.com
- **API base URL:** `https://api.tarvent.com`

## Authentication

### API Key

Connect Tarvent with an API key and the required account ID.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your Tarvent account ID from Account > Overview.

Send these headers with each API request:

```http
Account: <accountId>
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.tarvent.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/account) |
| [Get Account API Key](actions/get-account-api-key.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/accountApiKey) |
| [Get Account Invoice](actions/get-account-invoice.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/accountInvoice) |
| [Get Monthly Growth Stats](actions/get-monthly-growth-stats.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/accountMonthlyGrowthStats) |
| [List Account API Keys](actions/list-account-api-keys.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allAccountApiKeys) |
| [List Account Invoices](actions/list-account-invoices.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/accountInvoices) |
| [List Account Plan Stats](actions/list-account-plan-stats.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allAccountPlanStats) |
| [List Audiences](actions/list-audiences.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/audiences) |
| [List Campaigns](actions/list-campaigns.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/campaigns) |
| [List Custom Reports](actions/list-custom-reports.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allCustomReports) |
| [List Exports](actions/list-exports.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allExports) |
| [List Integration Partners](actions/list-integration-partners.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allIntegrationPartners) |
| [List Journeys](actions/list-journeys.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/journeys) |
| [List Plans](actions/list-plans.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allPlans) |
| [List Suppression Filters](actions/list-suppression-filters.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/accountSuppressionFilters) |
| [List Templates](actions/list-templates.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/templates) |
| [List Transactions](actions/list-transactions.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allTransactions) |
| [List User Notifications](actions/list-user-notifications.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allUserNotifications) |
| [List Webhooks](actions/list-webhooks.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allWebhooks) |
| [Search Account Entities](actions/search-account-entities.md) | `POST /graphql` | [docs](https://developer.tarvent.com/queries/allAccountEntities) |
