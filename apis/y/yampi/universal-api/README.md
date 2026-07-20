# <img src="https://images.mindcloud.co/apps/icons/yampi_1776713070576.png" alt="Yampi logo" width="28" height="28"> Yampi: Universal API

Yampi app built on the official REST API using direct API credentials (Alias, User Token, and User Secret Key).

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yampi/latest
- **Category:** Commerce
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.yampi.com.br/
- **Vendor API docs:** https://docs.yampi.com.br/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Address](actions/get-customer-address.md) | GET | Retrieves the specified customer address from Yampi. |
| [List Customer Addresses](actions/list-customer-addresses.md) | GET | Retrieves the addresses for a customer in Yampi. |
| [List Order Addresses](actions/list-order-addresses.md) | GET | Retrieves the addresses for an order in Yampi. |

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | GET | Retrieves the specified brand from Yampi. |
| [List Brands](actions/list-brands.md) | GET | Retrieves a list of brands from Yampi. |

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Carts](actions/list-customer-carts.md) | GET | Retrieves abandoned carts for a customer in Yampi. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves the specified category from Yampi. |
| [List Categories](actions/list-categories.md) | GET | Retrieves a list of categories from Yampi. |

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [List Checkout Config](actions/list-checkout-config.md) | GET | Retrieves the checkout configuration from Yampi. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Customizations](actions/list-customizations.md) | GET | Retrieves a list of customizations from Yampi. |

### Customer Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Filters](actions/list-customer-filters.md) | GET | Retrieves customer search filters from Yampi. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves the specified customer from Yampi. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Yampi. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [List Product Stocks](actions/list-product-stocks.md) | GET | Retrieves SKU stock levels for a product in Yampi. |

### Lead Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Filters](actions/list-lead-filters.md) | GET | Retrieves lead search filters from Yampi. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET | Retrieves the specified lead from Yampi. |
| [List Leads](actions/list-leads.md) | GET | Retrieves a list of leads from Yampi. |

### Order Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Order Filters](actions/list-order-filters.md) | GET | Retrieves order search filters from Yampi. |

### Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [List Order Items](actions/list-order-items.md) | GET | Retrieves the items for an order in Yampi. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves the specified order from Yampi. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Yampi. |

### Product Combo

| Action | Method | Description |
| --- | --- | --- |
| [List Product Combos](actions/list-product-combos.md) | GET | Retrieves the combos for a product in Yampi. |

### Product Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Product Comments](actions/list-product-comments.md) | GET | Retrieves a list of product comments from Yampi. |

### Product Promotion

| Action | Method | Description |
| --- | --- | --- |
| [List Product Promotions](actions/list-product-promotions.md) | GET | Retrieves the promotions for a product in Yampi. |

### Product Review

| Action | Method | Description |
| --- | --- | --- |
| [List Product Reviews](actions/list-product-reviews.md) | GET | Retrieves the reviews for a product in Yampi. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [List Product SKUs](actions/list-product-skus.md) | GET | Retrieves the SKUs for a product in Yampi. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves public product details from Yampi by slug. |
| [List Category Products](actions/list-category-products.md) | GET | Retrieves products assigned to a category in Yampi. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Yampi. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [List Order Tracking](actions/list-order-tracking.md) | GET | Retrieves tracking details for an order in Yampi. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Yampi. |

