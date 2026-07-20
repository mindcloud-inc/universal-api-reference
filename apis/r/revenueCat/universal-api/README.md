# <img src="https://images.mindcloud.co/apps/icons/revenuecat-icon_1776711610698.png" alt="RevenueCat logo" width="28" height="28"> RevenueCat: Universal API

RevenueCat is a subscription and in-app purchase platform for managing projects, apps, products, offerings, entitlements, customers, metrics, integrations, and purchase lifecycle operations through the RevenueCat REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/revenueCat/latest
- **Actions:** 95
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.revenuecat.com
- **Vendor API docs:** https://www.revenuecat.com/docs/api-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (95)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Create App](actions/create-app.md) | POST | Creates a new app in RevenueCat. |
| [Delete App](actions/delete-app.md) | DELETE | Deletes an existing app from RevenueCat. |
| [Get App](actions/get-app.md) | GET | Retrieves an app from RevenueCat. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from RevenueCat. |
| [Update App](actions/update-app.md) | PUT | Updates an existing app in RevenueCat. |

### App Public Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get App Public API Keys](actions/get-app-public-api-keys.md) | GET | Retrieves app public API keys from RevenueCat. |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET | Retrieves audit logs from RevenueCat. |

### Chart

| Action | Method | Description |
| --- | --- | --- |
| [Get Chart Data](actions/get-chart-data.md) | GET | Retrieves chart data from RevenueCat. |

### Chart Option

| Action | Method | Description |
| --- | --- | --- |
| [Get Chart Options](actions/get-chart-options.md) | GET | Retrieves chart options from RevenueCat. |

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET | Retrieves collaborators from RevenueCat. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in RevenueCat. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from RevenueCat. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from RevenueCat. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from RevenueCat. |

### Customer Alias

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Aliases](actions/get-customer-aliases.md) | GET | Retrieves a customer's aliases from RevenueCat. |

### Customer Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Attributes](actions/get-customer-attributes.md) | GET | Retrieves a customer's attributes from RevenueCat. |
| [Set Customer Attributes](actions/set-customer-attributes.md) | PUT | Updates a customer's attributes in RevenueCat. |

### Customer Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Active Entitlements](actions/get-customer-active-entitlements.md) | GET | Retrieves a customer's active entitlements from RevenueCat. |

### Customer Offering Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Customer Offering](actions/assign-customer-offering.md) | PUT | Assigns or clears a customer offering override in RevenueCat. |

### Customer Transfer

| Action | Method | Description |
| --- | --- | --- |
| [Transfer Customer](actions/transfer-customer.md) | PUT | Transfers a customer's subscriptions and purchases to another RevenueCat customer. |

### Customer Virtual Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Virtual Currencies](actions/get-customer-virtual-currencies.md) | GET | Retrieves a customer's virtual currency balances from RevenueCat. |

### Customer Virtual Currency Balance

| Action | Method | Description |
| --- | --- | --- |
| [Update Customer Virtual Currency Balance](actions/update-customer-virtual-currency-balance.md) | PUT | Updates a virtual currency balance in RevenueCat without a transaction. |

### Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [Archive Entitlement](actions/archive-entitlement.md) | PUT | Archives an entitlement in RevenueCat. |
| [Create Entitlement](actions/create-entitlement.md) | POST | Creates a new entitlement in RevenueCat. |
| [Delete Entitlement](actions/delete-entitlement.md) | DELETE | Deletes an existing entitlement from RevenueCat. |
| [Get Entitlement](actions/get-entitlement.md) | GET | Retrieves an entitlement from RevenueCat. |
| [List Entitlements](actions/list-entitlements.md) | GET | Retrieves entitlements from RevenueCat. |
| [Unarchive Entitlement](actions/unarchive-entitlement.md) | PUT | Unarchives an entitlement in RevenueCat. |
| [Update Entitlement](actions/update-entitlement.md) | PUT | Updates an existing entitlement in RevenueCat. |

### Entitlement Product Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Attach Products To Entitlement](actions/attach-products-to-entitlement.md) | PUT | Attaches products to an entitlement in RevenueCat. |

### Entitlement Product Detachment

| Action | Method | Description |
| --- | --- | --- |
| [Detach Products From Entitlement](actions/detach-products-from-entitlement.md) | PUT | Detaches products from an entitlement in RevenueCat. |

### Granted Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [Grant Customer Entitlement](actions/grant-customer-entitlement.md) | POST | Grants an entitlement to a RevenueCat customer. |

### Granted Entitlement Revocation

| Action | Method | Description |
| --- | --- | --- |
| [Revoke Granted Customer Entitlement](actions/revoke-granted-customer-entitlement.md) | DELETE | Revokes a granted customer entitlement in RevenueCat. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Invoices](actions/list-customer-invoices.md) | GET | Retrieves a customer's invoices from RevenueCat. |

### Invoice File

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Invoice File](actions/get-customer-invoice-file.md) | GET | Retrieves a customer invoice file from RevenueCat. |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Overview Metrics](actions/get-overview-metrics.md) | GET | Retrieves overview metrics from RevenueCat. |

### Offering

| Action | Method | Description |
| --- | --- | --- |
| [Archive Offering](actions/archive-offering.md) | PUT | Archives an offering in RevenueCat. |
| [Create Offering](actions/create-offering.md) | POST | Creates a new offering in RevenueCat. |
| [Delete Offering](actions/delete-offering.md) | DELETE | Deletes an offering and packages from RevenueCat. |
| [Get Offering](actions/get-offering.md) | GET | Retrieves an offering from RevenueCat. |
| [List Offerings](actions/list-offerings.md) | GET | Retrieves offerings from RevenueCat. |
| [Unarchive Offering](actions/unarchive-offering.md) | PUT | Unarchives an offering in RevenueCat. |
| [Update Offering](actions/update-offering.md) | PUT | Updates an existing offering in RevenueCat. |

### Offering Package Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Attach Package To Offering](actions/attach-package-to-offering.md) | PUT |  |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Delete Package](actions/delete-package.md) | DELETE | Deletes an existing package from RevenueCat. |
| [Get Package](actions/get-package.md) | GET | Retrieves a package from RevenueCat. |
| [List Offering Packages](actions/list-offering-packages.md) | GET | Retrieves packages attached to an offering in RevenueCat. |
| [Update Package](actions/update-package.md) | PUT | Updates an existing package in RevenueCat. |

### Package Product Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Attach Products To Package](actions/attach-products-to-package.md) | PUT | Attaches products to a package in RevenueCat. |

### Package Product Detachment

| Action | Method | Description |
| --- | --- | --- |
| [Detach Products From Package](actions/detach-products-from-package.md) | PUT | Detaches products from a package in RevenueCat. |

### Paywall

| Action | Method | Description |
| --- | --- | --- |
| [Create Paywall](actions/create-paywall.md) | POST | Creates a new paywall in RevenueCat. |
| [Delete Paywall](actions/delete-paywall.md) | DELETE | Deletes an existing paywall from RevenueCat. |
| [Get Paywall](actions/get-paywall.md) | GET | Retrieves a paywall from RevenueCat. |
| [List Paywalls](actions/list-paywalls.md) | GET | Retrieves paywalls from RevenueCat. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Archive Product](actions/archive-product.md) | PUT | Archives a product in RevenueCat. |
| [Create Product](actions/create-product.md) | POST | Creates a new product in RevenueCat. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from RevenueCat. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from RevenueCat. |
| [List Entitlement Products](actions/list-entitlement-products.md) | GET | Retrieves products attached to an entitlement in RevenueCat. |
| [List Package Products](actions/list-package-products.md) | GET | Retrieves products attached to a package in RevenueCat. |
| [List Products](actions/list-products.md) | GET | Retrieves products from RevenueCat. |
| [Unarchive Product](actions/unarchive-product.md) | PUT | Unarchives a product in RevenueCat. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in RevenueCat. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in RevenueCat. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from RevenueCat. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase](actions/get-purchase.md) | GET | Retrieves a purchase from RevenueCat. |
| [List Customer Purchases](actions/list-customer-purchases.md) | GET | Retrieves a customer's purchases from RevenueCat. |
| [List Purchases](actions/list-purchases.md) | GET |  |

### Purchase Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [List Purchase Entitlements](actions/list-purchase-entitlements.md) | GET | Retrieves entitlements for a purchase in RevenueCat. |

### Purchase Refund

| Action | Method | Description |
| --- | --- | --- |
| [Refund Purchase](actions/refund-purchase.md) | PUT | Refunds a Web Billing purchase in RevenueCat. |

### Restored Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Restore Customer Purchase By Order ID](actions/restore-customer-purchase-by-order-id.md) | PUT | Restores a Google Play purchase by order ID in RevenueCat. |

### Store Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product In Store](actions/create-product-in-store.md) | POST | Pushes a product to the App Store in RevenueCat. |

### Storekit Config

| Action | Method | Description |
| --- | --- | --- |
| [Get App StoreKit Config](actions/get-app-store-kit-config.md) | GET | Retrieves an app StoreKit configuration from RevenueCat. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from RevenueCat. |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | GET | Retrieves a customer's subscriptions from RevenueCat. |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |

### Subscription Cancellation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an active Web Billing subscription in RevenueCat. |

### Subscription Entitlement

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Entitlements](actions/list-subscription-entitlements.md) | GET | Retrieves entitlements for a subscription in RevenueCat. |

### Subscription Management Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Authenticated Management URL](actions/get-subscription-authenticated-management-url.md) | GET | Retrieves an authenticated subscription management URL from RevenueCat. |

### Subscription Refund

| Action | Method | Description |
| --- | --- | --- |
| [Refund Subscription](actions/refund-subscription.md) | PUT | Refunds an active Web Billing subscription in RevenueCat. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Transactions](actions/list-subscription-transactions.md) | GET | Retrieves transactions for a subscription in RevenueCat. |

### Transaction Refund

| Action | Method | Description |
| --- | --- | --- |
| [Refund Subscription Transaction](actions/refund-subscription-transaction.md) | PUT | Refunds a Play Store or Galaxy subscription transaction in RevenueCat. |

### Virtual Currency

| Action | Method | Description |
| --- | --- | --- |
| [Archive Virtual Currency](actions/archive-virtual-currency.md) | PUT | Archives a virtual currency in RevenueCat. |
| [Create Virtual Currency](actions/create-virtual-currency.md) | POST | Creates a new virtual currency in RevenueCat. |
| [Delete Virtual Currency](actions/delete-virtual-currency.md) | DELETE | Deletes an existing virtual currency from RevenueCat. |
| [Get Virtual Currency](actions/get-virtual-currency.md) | GET | Retrieves a virtual currency from RevenueCat. |
| [List Virtual Currencies](actions/list-virtual-currencies.md) | GET | Retrieves virtual currencies from RevenueCat. |
| [Unarchive Virtual Currency](actions/unarchive-virtual-currency.md) | PUT | Unarchives a virtual currency in RevenueCat. |
| [Update Virtual Currency](actions/update-virtual-currency.md) | PUT | Updates an existing virtual currency in RevenueCat. |

### Virtual Currency Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Virtual Currency Transaction](actions/create-customer-virtual-currency-transaction.md) | POST | Creates a virtual currency transaction in RevenueCat. |

### Webhook Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Integration](actions/create-webhook-integration.md) | POST | Creates a new webhook integration in RevenueCat. |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | DELETE | Deletes an existing webhook integration from RevenueCat. |
| [Get Webhook Integration](actions/get-webhook-integration.md) | GET | Retrieves a webhook integration from RevenueCat. |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | GET | Retrieves webhook integrations from RevenueCat. |
| [Update Webhook Integration](actions/update-webhook-integration.md) | PUT | Updates an existing webhook integration in RevenueCat. |

