# <img src="https://images.mindcloud.co/apps/icons/advant-shop_1776461106480.png" alt="AdvantShop logo" width="28" height="28"> AdvantShop: Universal API

AdvantShop store API wrapper for orders, customers, catalog, products, categories, leads, bonus cards, and storefront data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/advantShop/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.advantshop.net
- **Vendor API docs:** https://www.advantshop.net/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Initialize Store](actions/initialize-store.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/initialize-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog](actions/get-catalog.md) | GET | Retrieves the catalog from AdvantShop. |
| [Get Catalog Filter](actions/get-catalog-filter.md) | GET | Retrieves catalog filters from AdvantShop. |
| [Get Full Catalog](actions/get-full-catalog.md) | GET | Retrieves the full catalog from AdvantShop. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in AdvantShop. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from AdvantShop. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from AdvantShop. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in AdvantShop. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Product Reviews](actions/list-product-reviews.md) | GET | Retrieves product reviews from AdvantShop. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Carousels](actions/list-carousels.md) | GET | Retrieves carousel slides from AdvantShop. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in AdvantShop. |
| [Get Bonus Card](actions/get-bonus-card.md) | GET | Retrieves a bonus card from AdvantShop. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from AdvantShop. |
| [Get Customer Bonuses](actions/get-customer-bonuses.md) | GET | Retrieves a customer's bonus card from AdvantShop. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from AdvantShop. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in AdvantShop. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Groups](actions/list-customer-groups.md) | GET | Retrieves customer groups from AdvantShop. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [List Product Stocks](actions/list-product-stocks.md) | GET | Retrieves product stock levels from AdvantShop. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in AdvantShop. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from AdvantShop. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Change Order Status](actions/change-order-status.md) | PUT | Updates an order status in AdvantShop. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from AdvantShop. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from AdvantShop. |
| [Set Order Paid](actions/set-order-paid.md) | PUT | Marks an order as paid in AdvantShop. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Product Price](actions/calculate-product-price.md) | GET | Calculates a product price in AdvantShop. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Search](actions/autocomplete-search.md) | GET | Finds product and category matches in AdvantShop. |
| [Count Catalog Filter Products](actions/count-catalog-filter-products.md) | GET | Retrieves the product count for a catalog filter in AdvantShop. |
| [Count Search Filter Products](actions/count-search-filter-products.md) | GET | Retrieves the product count for a search filter in AdvantShop. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from AdvantShop. |
| [Get Product Properties](actions/get-product-properties.md) | GET | Retrieves product properties from AdvantShop. |
| [Get Search Filter](actions/get-search-filter.md) | GET | Retrieves search filters from AdvantShop. |
| [List Product Gifts](actions/list-product-gifts.md) | GET | Retrieves product gifts from AdvantShop. |
| [List Related Products](actions/list-related-products.md) | GET | Retrieves related products from AdvantShop. |
| [Search Catalog](actions/search-catalog.md) | GET | Finds product and category matches in AdvantShop. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves order statuses from AdvantShop. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Bonus Card Transactions](actions/list-bonus-card-transactions.md) | GET | Retrieves bonus card transactions from AdvantShop. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Bonus Card Settings](actions/get-bonus-card-settings.md) | GET | Retrieves bonus card settings from AdvantShop. |
| [Get Settings](actions/get-settings.md) | GET | Retrieves settings from AdvantShop. |
| [Initialize Store](actions/initialize-store.md) | GET | Retrieves store initialization data from AdvantShop. |
| [List Bonus Grades](actions/list-bonus-grades.md) | GET | Retrieves bonus grades from AdvantShop. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Managers](actions/list-managers.md) | GET | Retrieves managers from AdvantShop. |

