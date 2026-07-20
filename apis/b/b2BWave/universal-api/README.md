# <img src="https://images.mindcloud.co/apps/icons/5e2ec9c05b8bed8f33bd4eb4-favicon_1777490028969.jpeg" alt="B2B Wave logo" width="28" height="28"> B2B Wave: Universal API

Manage wholesale products, customers, pricing, and orders.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/b2BWave/latest
- **Category:** Commerce
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.b2bwave.com/
- **Vendor API docs:** https://docs.b2bwave.com/category/97-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves customer addresses from B2B Wave. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from B2B Wave. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Options](actions/list-options.md) | GET | Retrieves product options and values from B2B Wave. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from B2B Wave. |

### Discounts

| Action | Method | Description |
| --- | --- | --- |
| [List Product Discounts](actions/list-product-discounts.md) | GET | Retrieves product discounts from B2B Wave. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from B2B Wave. |

### Price Books

| Action | Method | Description |
| --- | --- | --- |
| [List Price Lists](actions/list-price-lists.md) | GET | Retrieves price lists from B2B Wave. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [List Product Customer Prices](actions/list-product-customer-prices.md) | GET | Retrieves customer-specific product prices from B2B Wave. |
| [List Product Prices](actions/list-product-prices.md) | GET | Retrieves product prices from B2B Wave. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves product variants from B2B Wave. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from B2B Wave. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Options](actions/list-shipping-options.md) | GET | Retrieves shipping options from B2B Wave. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves order statuses from B2B Wave. |
| [List Product Statuses](actions/list-product-statuses.md) | GET | Retrieves product statuses from B2B Wave. |

### Tax Codes

| Action | Method | Description |
| --- | --- | --- |
| [List VAT Classes](actions/list-vat-classes.md) | GET | Retrieves VAT classes from B2B Wave. |
| [List VAT Groups](actions/list-vat-groups.md) | GET | Retrieves VAT groups from B2B Wave. |
| [List VAT Rules](actions/list-vat-rules.md) | GET | Retrieves VAT rules from B2B Wave. |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [List VAT Rates](actions/list-vat-rates.md) | GET | Retrieves VAT rates from B2B Wave. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Reps](actions/list-sales-reps.md) | GET | Retrieves sales reps from B2B Wave. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from B2B Wave. |

