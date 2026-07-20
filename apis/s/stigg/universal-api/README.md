# <img src="https://images.mindcloud.co/apps/icons/stigg_1776872230622.png" alt="Stigg logo" width="28" height="28"> Stigg: Universal API

Stigg is a pricing, packaging, entitlements, subscriptions, and usage metering platform with a GraphQL API for managing customers, subscriptions, product catalog entities, entitlements, and billing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stigg/latest
- **Category:** Commerce
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.stigg.io
- **Vendor API docs:** https://docs.stigg.io/api-and-sdks/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [API Key Scope](actions/api-key-scope.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Addon

| Action | Method | Description |
| --- | --- | --- |
| [Create One Addon](actions/create-one-addon.md) | POST |  |
| [Get Addon By Ref ID](actions/get-addon-by-ref-id.md) | GET |  |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [API Key Scope](actions/api-key-scope.md) | GET |  |
| [List API Keys](actions/api-keys.md) | GET |  |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Integrations](actions/integrations.md) | GET |  |

### Available Scope

| Action | Method | Description |
| --- | --- | --- |
| [Available Scopes](actions/available-scopes.md) | GET |  |

### Bulk Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Report Usage Bulk](actions/report-usage-bulk.md) | POST |  |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Get Coupon](actions/get-coupon.md) | GET |  |
| [List Coupons](actions/list-coupons.md) | GET |  |

### Credit Grant

| Action | Method | Description |
| --- | --- | --- |
| [Credit Grants](actions/credit-grants.md) | GET |  |

### Credit Usage

| Action | Method | Description |
| --- | --- | --- |
| [Credit Usage](actions/credit-usage.md) | GET |  |

### Credits Ledger

| Action | Method | Description |
| --- | --- | --- |
| [Credits Ledger](actions/credits-ledger.md) | GET |  |

### Custom Currency

| Action | Method | Description |
| --- | --- | --- |
| [Custom Currencies](actions/custom-currencies.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Update One Customer](actions/update-one-customer.md) | PUT |  |

### Customer Portal

| Action | Method | Description |
| --- | --- | --- |
| [Customer Portal](actions/customer-portal.md) | GET |  |

### Customer Provisioning

| Action | Method | Description |
| --- | --- | --- |
| [Provision Customer](actions/provision-customer.md) | POST |  |

### Customer Resource

| Action | Method | Description |
| --- | --- | --- |
| [Customer Resources](actions/customer-resources.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer By Ref ID](actions/get-customer-by-ref-id.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |

### Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [Get Entitlement](actions/get-entitlement.md) | GET |  |
| [Get Entitlements With Summary](actions/get-entitlements-with-summary.md) | GET |  |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Environments](actions/environments.md) | GET |  |
| [Get Current Environment](actions/get-current-environment.md) | GET |  |

### Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Event Logs](actions/event-logs.md) | GET |  |

### Event Report

| Action | Method | Description |
| --- | --- | --- |
| [Report Event](actions/report-event.md) | POST |  |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Experiment](actions/experiment.md) | GET |  |
| [Experiments](actions/experiments.md) | GET |  |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [List Features](actions/features.md) | GET |  |

### Feature Group

| Action | Method | Description |
| --- | --- | --- |
| [List Feature Groups](actions/list-feature-groups.md) | GET |  |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Offer](actions/get-offer.md) | GET |  |
| [Offers](actions/offers.md) | GET |  |

### Package Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [Package Entitlements](actions/package-entitlements.md) | GET |  |

### Package Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Package Group](actions/get-package-group.md) | GET |  |
| [List Package Groups](actions/list-package-groups.md) | GET |  |
| [Package Group](actions/package-group.md) | GET |  |

### Payment Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Session](actions/create-payment-session.md) | POST |  |

### Paywall

| Action | Method | Description |
| --- | --- | --- |
| [Get Paywall](actions/paywall.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create One Plan](actions/create-one-plan.md) | POST |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create One Product](actions/create-one-product.md) | POST |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET |  |

### Sdk Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get SDK Configuration](actions/sdk-configuration.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Update One Subscription](actions/update-one-subscription.md) | PUT |  |

### Subscription Cancellation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan By Ref ID](actions/get-plan-by-ref-id.md) | GET |  |
| [List Addons](actions/list-addons.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |

### Subscription Provisioning

| Action | Method | Description |
| --- | --- | --- |
| [Provision Subscription](actions/provision-subscription.md) | POST |  |

### Subscription Provisioning V2

| Action | Method | Description |
| --- | --- | --- |
| [Provision Subscription V2](actions/provision-subscription-v2.md) | POST |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Subscriptions](actions/get-active-subscriptions.md) | GET |  |
| [Get Subscription](actions/get-subscription.md) | GET |  |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |

### Usage Event

| Action | Method | Description |
| --- | --- | --- |
| [List Usage Events](actions/list-usage-events.md) | GET |  |

### Usage History

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage History](actions/get-usage-history.md) | GET |  |

### Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Report Usage](actions/report-usage.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Current User](actions/current-user.md) | GET |  |
| [Members](actions/members.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Hook](actions/hook.md) | GET |  |
| [Hooks](actions/hooks.md) | GET |  |

