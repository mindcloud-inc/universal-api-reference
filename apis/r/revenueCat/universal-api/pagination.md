# RevenueCat Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model RevenueCat expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/get-app-public-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## RevenueCat actions that support pagination

- [Get App Public API Keys](actions/get-app-public-api-keys.md)
- [Get Customer Active Entitlements](actions/get-customer-active-entitlements.md)
- [Get Customer Aliases](actions/get-customer-aliases.md)
- [Get Customer Attributes](actions/get-customer-attributes.md)
- [Get Customer Virtual Currencies](actions/get-customer-virtual-currencies.md)
- [List Apps](actions/list-apps.md)
- [List Audit Logs](actions/list-audit-logs.md)
- [List Collaborators](actions/list-collaborators.md)
- [List Customer Invoices](actions/list-customer-invoices.md)
- [List Customer Purchases](actions/list-customer-purchases.md)
- [List Customer Subscriptions](actions/list-customer-subscriptions.md)
- [List Customers](actions/list-customers.md)
- [List Entitlement Products](actions/list-entitlement-products.md)
- [List Entitlements](actions/list-entitlements.md)
- [List Offering Packages](actions/list-offering-packages.md)
- [List Offerings](actions/list-offerings.md)
- [List Package Products](actions/list-package-products.md)
- [List Paywalls](actions/list-paywalls.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
- [List Purchase Entitlements](actions/list-purchase-entitlements.md)
- [List Purchases](actions/list-purchases.md)
- [List Subscription Entitlements](actions/list-subscription-entitlements.md)
- [List Subscription Transactions](actions/list-subscription-transactions.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Virtual Currencies](actions/list-virtual-currencies.md)
- [List Webhook Integrations](actions/list-webhook-integrations.md)
