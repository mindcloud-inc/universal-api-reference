# Nautical: Native API Reference

A consolidated summary of Nautical's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://guide.thetraide.com/docs/api/
- **OpenAPI specification:** https://api.mpconsole.com/graphql/
- **API base URL:** `https://api.mpconsole.com`

## Authentication

### API Key

Use a Nautical custom-app bearer token. Requests also require the tenant header configured on the app API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://guide.thetraide.com/docs/users-guide/apps/algolia/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/apps/) |
| [List Attribute Values](actions/list-attribute-values.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/attribute-values/) |
| [List Attributes](actions/list-attributes.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/attributes/) |
| [List Avalara Request Logs](actions/list-avalara-request-logs.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/avalara-request-logs/) |
| [List Checkout Events](actions/list-checkout-events.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/checkout-events/) |
| [List Checkout Lines](actions/list-checkout-lines.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/checkout-lines/) |
| [List Checkouts](actions/list-checkouts.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/checkouts/) |
| [List Collections](actions/list-collections.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/collections/) |
| [List Content](actions/list-content.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/content-list/) |
| [List Countries](actions/list-countries.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/countries/) |
| [List Currencies](actions/list-currencies.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/currencies/) |
| [List Customers](actions/list-customers.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/customers/) |
| [List Digital Contents](actions/list-digital-contents.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/digital-contents/) |
| [List Draft Orders](actions/list-draft-orders.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/draft-orders/) |
| [List Email Logs](actions/list-email-logs.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/email-logs/) |
| [List Email Templates](actions/list-email-templates.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/email-templates/) |
| [List Export Files](actions/list-export-files.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/export-files/) |
| [List Import Files](actions/list-import-files.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/import-files/) |
| [List Marketplace Subscriptions](actions/list-marketplace-subscriptions.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/marketplace-subscriptions/) |
| [List Media](actions/list-media.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/media-list/) |
| [List Menu Items](actions/list-menu-items.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/menu-items/) |
| [List Menus](actions/list-menus.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/menus/) |
| [List Nautical Orders](actions/list-nautical-orders.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/nautical-orders/) |
| [List Orders](actions/list-orders.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/orders/) |
| [List Payments](actions/list-payments.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/payments/) |
| [List Payouts](actions/list-payouts.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/payouts/) |
| [List Permission Groups](actions/list-permission-groups.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/permission-groups/) |
| [List Plugins](actions/list-plugins.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/plugins/) |
| [List Product Types](actions/list-product-types.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/product-types/) |
| [List Product Variants](actions/list-product-variants.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/product-variants/) |
| [List Products](actions/list-products.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/products/) |
| [List Refunds](actions/list-refunds.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/refunds/) |
| [List Returns](actions/list-returns.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/returns/) |
| [List Sales](actions/list-sales.md) | `POST graphql/` | [docs](https://guide.thetraide.com/docs/api/operations/queries/sales/) |
