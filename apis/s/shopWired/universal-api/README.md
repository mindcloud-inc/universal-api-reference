# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-21-as-17_1776801957991.png" alt="ShopWired logo" width="28" height="28"> ShopWired: Universal API

Build e-commerce automations for ShopWired stores, including products, orders, customers, catalog data, stock, and store metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shopWired/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shopwired.co.uk
- **Vendor API docs:** https://shopwired.readme.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve business details](actions/get-business.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-business?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific category](actions/get-category-by-id.md) | GET | Retrieves a category from ShopWired by ID. |
| [Get total category count](actions/get-category-count.md) | GET | Retrieves the total category count from ShopWired. |
| [List categories](actions/list-categories.md) | GET | Retrieves categories from ShopWired. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve business details](actions/get-business.md) | GET | Retrieves business details from ShopWired. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List product customisation fields](actions/list-product-customization-fields.md) | GET | Retrieves customisation fields for a product from ShopWired. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific customer](actions/get-customer-by-id.md) | GET | Retrieves a customer from ShopWired by ID. |
| [Get total customer count](actions/get-customer-count.md) | GET | Retrieves the total customer count from ShopWired. |
| [List customers](actions/list-customers.md) | GET | Retrieves customers from ShopWired. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List product images](actions/list-product-images.md) | GET | Retrieves images for a product from ShopWired. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve stock quantity](actions/get-stock.md) | GET | Retrieves stock quantities from ShopWired by SKU. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific country](actions/get-country-by-id.md) | GET | Retrieves a country from ShopWired by ID. |
| [List countries](actions/list-countries.md) | GET | Retrieves countries from ShopWired. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get an incomplete order by ID](actions/get-incomplete-order.md) | GET | Retrieves an incomplete order from ShopWired by ID. |
| [Get total incomplete order count](actions/get-incomplete-order-count.md) | GET | Retrieves the total incomplete order count from ShopWired. |
| [Get an order by ID](actions/get-order.md) | GET | Retrieves an order from ShopWired by ID. |
| [Get order count](actions/get-order-count.md) | GET | Retrieves the total order count from ShopWired. |
| [List incomplete orders](actions/list-incomplete-orders.md) | GET | Retrieves incomplete orders from ShopWired. |
| [List orders](actions/list-orders.md) | GET | Retrieves orders from ShopWired. |
| [Search for orders](actions/search-orders.md) | GET | Finds orders in ShopWired by keyword. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List external payment methods](actions/list-payment-methods.md) | GET | Retrieves external payment methods from ShopWired. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific product variation](actions/get-product-variation-by-id.md) | GET | Retrieves a product variation from ShopWired by ID. |
| [List product variations](actions/list-product-variations.md) | GET | Retrieves variations for a product from ShopWired. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get a single product](actions/get-product-by-id.md) | GET | Retrieves a product from ShopWired by ID. |
| [List products](actions/list-products.md) | GET | Retrieves products from ShopWired. |
| [Search products](actions/search-products.md) | GET | Finds products in ShopWired by keyword. |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [List product reviews](actions/list-product-reviews.md) | GET | Retrieves reviews for a product from ShopWired. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List order statuses](actions/list-order-statuses.md) | GET | Retrieves order statuses from ShopWired. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific newsletter subscriber](actions/get-newsletter-subscriber.md) | GET | Retrieves a newsletter subscriber from ShopWired by ID. |
| [List newsletter subscribers](actions/list-newsletter-subscribers.md) | GET | Retrieves newsletter subscribers from ShopWired. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific brand](actions/get-brand-by-id.md) | GET | Retrieves a brand from ShopWired by ID. |
| [Get total brand count](actions/get-brand-count.md) | GET | Retrieves the total brand count from ShopWired. |
| [Get total filter group count](actions/get-filter-group-count.md) | GET | Retrieves the total filter group count from ShopWired. |
| [Get a product choice](actions/get-product-choice.md) | GET | Retrieves a product choice from ShopWired by ID. |
| [Get a product option](actions/get-product-option-by-id.md) | GET | Retrieves a product option from ShopWired by ID. |
| [List active brands](actions/list-brands.md) | GET | Retrieves active brands from ShopWired. |
| [List business features](actions/list-business-features.md) | GET | Retrieves enabled business features from ShopWired. |
| [List filter groups](actions/list-filter-groups.md) | GET | Retrieves filter groups from ShopWired. |
| [List product choices](actions/list-product-choices.md) | GET | Retrieves choices for a product from ShopWired. |
| [List product extras](actions/list-product-extras.md) | GET | Retrieves extras for a product from ShopWired. |
| [List product options](actions/list-product-options.md) | GET | Retrieves options for a product from ShopWired. |

