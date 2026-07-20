# RevenueCat: Native API Reference

A consolidated summary of RevenueCat's API configuration and 95 documented operations, with links to official documentation.

- **Official docs:** https://www.revenuecat.com/docs/api-v2
- **API base URL:** `https://api.revenuecat.com/v2`

## Authentication

### RevenueCat API Key

RevenueCat REST API v2 secret API key. Requests are authenticated with Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.revenuecat.com/docs/projects/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Endpoints (95 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Entitlement](actions/archive-entitlement.md) | `POST projects/:projectId/entitlements/:entitlementId/actions/archive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Archive Offering](actions/archive-offering.md) | `POST projects/:projectId/offerings/:offeringId/actions/archive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Archive Product](actions/archive-product.md) | `POST projects/:projectId/products/:productId/actions/archive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Archive Virtual Currency](actions/archive-virtual-currency.md) | `POST projects/:projectId/virtual_currencies/:virtualCurrencyCode/actions/archive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Assign Customer Offering](actions/assign-customer-offering.md) | `POST projects/:projectId/customers/:customerId/actions/assign_offering` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Attach Package To Offering](actions/attach-package-to-offering.md) | `POST projects/:projectId/offerings/:offeringId/packages` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Attach Products To Entitlement](actions/attach-products-to-entitlement.md) | `POST projects/:projectId/entitlements/:entitlementId/actions/attach_products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Attach Products To Package](actions/attach-products-to-package.md) | `POST projects/:projectId/packages/:packageId/actions/attach_products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST projects/:projectId/subscriptions/:subscriptionId/actions/cancel` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create App](actions/create-app.md) | `POST projects/:projectId/apps` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Customer](actions/create-customer.md) | `POST projects/:projectId/customers` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Customer Virtual Currency Transaction](actions/create-customer-virtual-currency-transaction.md) | `POST projects/:projectId/customers/:customerId/virtual_currencies/transactions` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Entitlement](actions/create-entitlement.md) | `POST projects/:projectId/entitlements` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Offering](actions/create-offering.md) | `POST projects/:projectId/offerings` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Paywall](actions/create-paywall.md) | `POST projects/:projectId/paywalls` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Product](actions/create-product.md) | `POST projects/:projectId/products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Product In Store](actions/create-product-in-store.md) | `POST projects/:projectId/products/:productId/create_in_store` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Virtual Currency](actions/create-virtual-currency.md) | `POST projects/:projectId/virtual_currencies` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Create Webhook Integration](actions/create-webhook-integration.md) | `POST projects/:projectId/integrations/webhooks` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete App](actions/delete-app.md) | `DELETE projects/:projectId/apps/:appId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Customer](actions/delete-customer.md) | `DELETE projects/:projectId/customers/:customerId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Entitlement](actions/delete-entitlement.md) | `DELETE projects/:projectId/entitlements/:entitlementId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Offering](actions/delete-offering.md) | `DELETE projects/:projectId/offerings/:offeringId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Package](actions/delete-package.md) | `DELETE projects/:projectId/packages/:packageId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Paywall](actions/delete-paywall.md) | `DELETE projects/:projectId/paywalls/:paywallId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Product](actions/delete-product.md) | `DELETE projects/:projectId/products/:productId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Virtual Currency](actions/delete-virtual-currency.md) | `DELETE projects/:projectId/virtual_currencies/:virtualCurrencyCode` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | `DELETE projects/:projectId/integrations/webhooks/:webhookIntegrationId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Detach Products From Entitlement](actions/detach-products-from-entitlement.md) | `POST projects/:projectId/entitlements/:entitlementId/actions/detach_products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Detach Products From Package](actions/detach-products-from-package.md) | `POST projects/:projectId/packages/:packageId/actions/detach_products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get App](actions/get-app.md) | `GET projects/:projectId/apps/:appId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get App Public API Keys](actions/get-app-public-api-keys.md) | `GET projects/:projectId/apps/:appId/public_api_keys` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get App StoreKit Config](actions/get-app-store-kit-config.md) | `GET projects/:projectId/apps/:appId/store_kit_config` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Chart Data](actions/get-chart-data.md) | `GET projects/:projectId/charts/:chartName` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Chart Options](actions/get-chart-options.md) | `GET projects/:projectId/charts/:chartName/options` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer](actions/get-customer.md) | `GET projects/:projectId/customers/:customerId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer Active Entitlements](actions/get-customer-active-entitlements.md) | `GET projects/:projectId/customers/:customerId/active_entitlements` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer Aliases](actions/get-customer-aliases.md) | `GET projects/:projectId/customers/:customerId/aliases` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer Attributes](actions/get-customer-attributes.md) | `GET projects/:projectId/customers/:customerId/attributes` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer Invoice File](actions/get-customer-invoice-file.md) | `GET projects/:projectId/customers/:customerId/invoices/:invoiceId/file` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Customer Virtual Currencies](actions/get-customer-virtual-currencies.md) | `GET projects/:projectId/customers/:customerId/virtual_currencies` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Entitlement](actions/get-entitlement.md) | `GET projects/:projectId/entitlements/:entitlementId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Offering](actions/get-offering.md) | `GET projects/:projectId/offerings/:offeringId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Overview Metrics](actions/get-overview-metrics.md) | `GET projects/:projectId/metrics/overview` | [docs](https://www.revenuecat.com/docs/api-v2#tag/Charts-and-Metrics) |
| [Get Package](actions/get-package.md) | `GET projects/:projectId/packages/:packageId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Paywall](actions/get-paywall.md) | `GET projects/:projectId/paywalls/:paywallId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Product](actions/get-product.md) | `GET projects/:projectId/products/:productId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Purchase](actions/get-purchase.md) | `GET projects/:projectId/purchases/:purchaseId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Subscription](actions/get-subscription.md) | `GET projects/:projectId/subscriptions/:subscriptionId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Subscription Authenticated Management URL](actions/get-subscription-authenticated-management-url.md) | `GET projects/:projectId/subscriptions/:subscriptionId/authenticated_management_url` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Virtual Currency](actions/get-virtual-currency.md) | `GET projects/:projectId/virtual_currencies/:virtualCurrencyCode` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Get Webhook Integration](actions/get-webhook-integration.md) | `GET projects/:projectId/integrations/webhooks/:webhookIntegrationId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Grant Customer Entitlement](actions/grant-customer-entitlement.md) | `POST projects/:projectId/customers/:customerId/actions/grant_entitlement` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Apps](actions/list-apps.md) | `GET projects/:projectId/apps` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET projects/:projectId/audit_logs` | [docs](https://www.revenuecat.com/docs/api-v2#tag/Audit-Log) |
| [List Collaborators](actions/list-collaborators.md) | `GET projects/:projectId/collaborators` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Customer Invoices](actions/list-customer-invoices.md) | `GET projects/:projectId/customers/:customerId/invoices` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Customer Purchases](actions/list-customer-purchases.md) | `GET projects/:projectId/customers/:customerId/purchases` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | `GET projects/:projectId/customers/:customerId/subscriptions` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Customers](actions/list-customers.md) | `GET projects/:projectId/customers` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Entitlement Products](actions/list-entitlement-products.md) | `GET projects/:projectId/entitlements/:entitlementId/products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Entitlements](actions/list-entitlements.md) | `GET projects/:projectId/entitlements` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Offering Packages](actions/list-offering-packages.md) | `GET projects/:projectId/offerings/:offeringId/packages` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Offerings](actions/list-offerings.md) | `GET projects/:projectId/offerings` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Package Products](actions/list-package-products.md) | `GET projects/:projectId/packages/:packageId/products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Paywalls](actions/list-paywalls.md) | `GET projects/:projectId/paywalls` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Products](actions/list-products.md) | `GET projects/:projectId/products` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Projects](actions/list-projects.md) | `GET projects` | [docs](https://www.revenuecat.com/docs/api-v2#tag/Project/operation/list-projects) |
| [List Purchase Entitlements](actions/list-purchase-entitlements.md) | `GET projects/:projectId/purchases/:purchaseId/entitlements` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Purchases](actions/list-purchases.md) | `GET projects/:projectId/purchases` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Subscription Entitlements](actions/list-subscription-entitlements.md) | `GET projects/:projectId/subscriptions/:subscriptionId/entitlements` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Subscription Transactions](actions/list-subscription-transactions.md) | `GET projects/:projectId/subscriptions/:subscriptionId/transactions` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET projects/:projectId/subscriptions` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Virtual Currencies](actions/list-virtual-currencies.md) | `GET projects/:projectId/virtual_currencies` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | `GET projects/:projectId/integrations/webhooks` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Refund Purchase](actions/refund-purchase.md) | `POST projects/:projectId/purchases/:purchaseId/actions/refund` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Refund Subscription](actions/refund-subscription.md) | `POST projects/:projectId/subscriptions/:subscriptionId/actions/refund` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Refund Subscription Transaction](actions/refund-subscription-transaction.md) | `POST projects/:projectId/subscriptions/:subscriptionId/transactions/:transactionId/actions/refund` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Restore Customer Purchase By Order ID](actions/restore-customer-purchase-by-order-id.md) | `POST projects/:projectId/customers/:customerId/actions/restore_purchase_by_order_id` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Revoke Granted Customer Entitlement](actions/revoke-granted-customer-entitlement.md) | `POST projects/:projectId/customers/:customerId/actions/revoke_granted_entitlement` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Set Customer Attributes](actions/set-customer-attributes.md) | `POST projects/:projectId/customers/:customerId/attributes` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Transfer Customer](actions/transfer-customer.md) | `POST projects/:projectId/customers/:customerId/actions/transfer` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Unarchive Entitlement](actions/unarchive-entitlement.md) | `POST projects/:projectId/entitlements/:entitlementId/actions/unarchive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Unarchive Offering](actions/unarchive-offering.md) | `POST projects/:projectId/offerings/:offeringId/actions/unarchive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Unarchive Product](actions/unarchive-product.md) | `POST projects/:projectId/products/:productId/actions/unarchive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Unarchive Virtual Currency](actions/unarchive-virtual-currency.md) | `POST projects/:projectId/virtual_currencies/:virtualCurrencyCode/actions/unarchive` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update App](actions/update-app.md) | `POST projects/:projectId/apps/:appId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Customer Virtual Currency Balance](actions/update-customer-virtual-currency-balance.md) | `POST projects/:projectId/customers/:customerId/virtual_currencies/update_balance` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Entitlement](actions/update-entitlement.md) | `POST projects/:projectId/entitlements/:entitlementId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Offering](actions/update-offering.md) | `POST projects/:projectId/offerings/:offeringId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Package](actions/update-package.md) | `POST projects/:projectId/packages/:packageId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Product](actions/update-product.md) | `POST projects/:projectId/products/:productId` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Virtual Currency](actions/update-virtual-currency.md) | `POST projects/:projectId/virtual_currencies/:virtualCurrencyCode` | [docs](https://www.revenuecat.com/docs/api-v2) |
| [Update Webhook Integration](actions/update-webhook-integration.md) | `POST projects/:projectId/integrations/webhooks/:webhookIntegrationId` | [docs](https://www.revenuecat.com/docs/api-v2) |
