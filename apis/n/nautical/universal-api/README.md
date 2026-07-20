# <img src="https://images.mindcloud.co/apps/icons/nautical_1775498488654.png" alt="Nautical logo" width="28" height="28"> Nautical: Universal API

Access Nautical marketplace data through the authenticated Traide GraphQL API using a tenant-specific bearer token and tenant header.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nautical/latest
- **Category:** Commerce
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thetraide.com/headless
- **Vendor API docs:** https://guide.thetraide.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### App

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET | Retrieves a list of apps from Nautical. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List Attributes](actions/list-attributes.md) | GET | Retrieves a list of attributes from Nautical. |

### Attribute Value

| Action | Method | Description |
| --- | --- | --- |
| [List Attribute Values](actions/list-attribute-values.md) | GET | Retrieves a list of attribute values from Nautical. |

### Avalara Request Log

| Action | Method | Description |
| --- | --- | --- |
| [List Avalara Request Logs](actions/list-avalara-request-logs.md) | GET | Retrieves a list of Avalara request logs from Nautical. |

### Checkout Event

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Events](actions/list-checkout-events.md) | GET | Retrieves a list of checkout events from Nautical. |

### Checkout Line

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Lines](actions/list-checkout-lines.md) | GET | Retrieves a list of checkout lines from Nautical. |

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [List Checkouts](actions/list-checkouts.md) | GET | Retrieves a list of checkouts from Nautical. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves a list of collections from Nautical. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [List Content](actions/list-content.md) | GET | Retrieves a list of content from Nautical. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves a list of countries from Nautical. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves a list of currencies from Nautical. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Nautical. |

### Digital Content

| Action | Method | Description |
| --- | --- | --- |
| [List Digital Contents](actions/list-digital-contents.md) | GET | Retrieves a list of digital contents from Nautical. |

### Draft Order

| Action | Method | Description |
| --- | --- | --- |
| [List Draft Orders](actions/list-draft-orders.md) | GET | Retrieves a list of draft orders from Nautical. |

### Email Log

| Action | Method | Description |
| --- | --- | --- |
| [List Email Logs](actions/list-email-logs.md) | GET | Retrieves a list of email logs from Nautical. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves a list of email templates from Nautical. |

### Export File

| Action | Method | Description |
| --- | --- | --- |
| [List Export Files](actions/list-export-files.md) | GET | Retrieves a list of export files from Nautical. |

### Import File

| Action | Method | Description |
| --- | --- | --- |
| [List Import Files](actions/list-import-files.md) | GET | Retrieves a list of import files from Nautical. |

### Marketplace Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Marketplace Subscriptions](actions/list-marketplace-subscriptions.md) | GET | Retrieves a list of marketplace subscriptions from Nautical. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [List Media](actions/list-media.md) | GET | Retrieves a list of media from Nautical. |

### Menu

| Action | Method | Description |
| --- | --- | --- |
| [List Menus](actions/list-menus.md) | GET | Retrieves a list of menus from Nautical. |

### Menu Item

| Action | Method | Description |
| --- | --- | --- |
| [List Menu Items](actions/list-menu-items.md) | GET | Retrieves a list of menu items from Nautical. |

### Nautical Order

| Action | Method | Description |
| --- | --- | --- |
| [List Nautical Orders](actions/list-nautical-orders.md) | GET | Retrieves a list of Nautical orders. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Nautical. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves a list of payments from Nautical. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves a list of payouts from Nautical. |

### Permission Group

| Action | Method | Description |
| --- | --- | --- |
| [List Permission Groups](actions/list-permission-groups.md) | GET | Retrieves a list of permission groups from Nautical. |

### Plugin

| Action | Method | Description |
| --- | --- | --- |
| [List Plugins](actions/list-plugins.md) | GET | Retrieves a list of plugins from Nautical. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Nautical. |

### Product Type

| Action | Method | Description |
| --- | --- | --- |
| [List Product Types](actions/list-product-types.md) | GET | Retrieves a list of product types from Nautical. |

### Product Variant

| Action | Method | Description |
| --- | --- | --- |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves a list of product variants from Nautical. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves a list of refunds from Nautical. |

### Return

| Action | Method | Description |
| --- | --- | --- |
| [List Returns](actions/list-returns.md) | GET | Retrieves a list of returns from Nautical. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [List Sales](actions/list-sales.md) | GET | Retrieves a list of sales from Nautical. |

