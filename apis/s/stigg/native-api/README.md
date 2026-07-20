# Stigg: Native API Reference

A consolidated summary of Stigg's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://docs.stigg.io/api-and-sdks/api-reference/overview
- **API base URL:** `https://api.stigg.io`

## Authentication

### API key

Stigg server API key sent in the X-API-Key header.

### Credentials

- **API key:** `apiKey` · required · Stigg Server API key for the target environment. Sent as the X-API-Key request header.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.stigg.io/api-and-sdks/api-reference/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [API Key Scope](actions/api-key-scope.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/apiKeyScope) |
| [List API Keys](actions/api-keys.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/apiKeys) |
| [Available Scopes](actions/available-scopes.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/availableScopes) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/cancelSubscription) |
| [Create One Addon](actions/create-one-addon.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/createOneAddon) |
| [Create One Plan](actions/create-one-plan.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/createOnePlan) |
| [Create One Product](actions/create-one-product.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/createOneProduct) |
| [Create Payment Session](actions/create-payment-session.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/createPaymentSession) |
| [Create Subscription](actions/create-subscription.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/createSubscription) |
| [Credit Grants](actions/credit-grants.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/creditGrants) |
| [Credit Usage](actions/credit-usage.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/creditUsage) |
| [Credits Ledger](actions/credits-ledger.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/creditsLedger) |
| [Current User](actions/current-user.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/currentUser) |
| [Custom Currencies](actions/custom-currencies.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/customCurrencies) |
| [Customer Portal](actions/customer-portal.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/customerPortal) |
| [Customer Resources](actions/customer-resources.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/customerResources) |
| [Environments](actions/environments.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/environments) |
| [Event Logs](actions/event-logs.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/eventLogs) |
| [Experiment](actions/experiment.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/experiment) |
| [Experiments](actions/experiments.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/experiments) |
| [List Features](actions/features.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/features) |
| [Get Active Subscriptions](actions/get-active-subscriptions.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getActiveSubscriptions) |
| [Get Addon By Ref ID](actions/get-addon-by-ref-id.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getAddonByRefId) |
| [Get Coupon](actions/get-coupon.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/coupon) |
| [Get Current Environment](actions/get-current-environment.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/currentEnvironment) |
| [Get Customer By Ref ID](actions/get-customer-by-ref-id.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getCustomerByRefId) |
| [Get Entitlement](actions/get-entitlement.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/entitlementV2) |
| [Get Entitlements With Summary](actions/get-entitlements-with-summary.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/entitlementsWithSummary) |
| [Get Offer](actions/get-offer.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getOffer) |
| [Get Package Group](actions/get-package-group.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getPackageGroup) |
| [Get Plan By Ref ID](actions/get-plan-by-ref-id.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getPlanByRefId) |
| [Get Subscription](actions/get-subscription.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/getSubscription) |
| [Get Usage History](actions/get-usage-history.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/usageHistoryV2) |
| [Hook](actions/hook.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/hook) |
| [Hooks](actions/hooks.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/hooks) |
| [Integrations](actions/integrations.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/integrations) |
| [List Addons](actions/list-addons.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/addons) |
| [List Coupons](actions/list-coupons.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/coupons) |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/customerSubscriptions) |
| [List Customers](actions/list-customers.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/customers) |
| [List Feature Groups](actions/list-feature-groups.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/featureGroups) |
| [List Package Groups](actions/list-package-groups.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/packageGroups) |
| [List Plans](actions/list-plans.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/plans) |
| [List Products](actions/list-products.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/products) |
| [List Subscriptions](actions/list-subscriptions.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/subscriptions) |
| [List Usage Events](actions/list-usage-events.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/usageEvents) |
| [Members](actions/members.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/members) |
| [Offers](actions/offers.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/offers) |
| [Package Entitlements](actions/package-entitlements.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/packageEntitlements) |
| [Package Group](actions/package-group.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/packageGroup) |
| [Get Paywall](actions/paywall.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/paywall) |
| [Provision Customer](actions/provision-customer.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/provisionCustomer) |
| [Provision Subscription](actions/provision-subscription.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/provisionSubscription) |
| [Provision Subscription V2](actions/provision-subscription-v2.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/provisionSubscriptionV2) |
| [Report Event](actions/report-event.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/reportEvent) |
| [Report Usage](actions/report-usage.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/reportUsage) |
| [Report Usage Bulk](actions/report-usage-bulk.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/reportUsageBulk) |
| [Get SDK Configuration](actions/sdk-configuration.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/queries/sdkConfiguration) |
| [Update One Customer](actions/update-one-customer.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/updateOneCustomer) |
| [Update One Subscription](actions/update-one-subscription.md) | `POST /graphql` | [docs](https://api-docs.stigg.io/mutations/updateOneSubscription) |
