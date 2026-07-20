# <img src="https://images.mindcloud.co/apps/icons/preview-emporix-commerce_1776090543946.png" alt="Emporix Commerce Engine logo" width="28" height="28"> Emporix Commerce Engine: Universal API

Emporix Commerce Engine provides REST APIs for managing commerce resources including products, catalogs, categories, carts, orders, prices, legal entities, and availability.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emporixCommerceEngine/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emporix.com
- **Vendor API docs:** https://developer.emporix.io/api-references/api-guides/api-guides-and-references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Add Cart Item](actions/add-cart-item.md) | POST | Adds an item to a cart in Emporix Commerce Engine. |
| [Create Cart](actions/create-cart.md) | POST | Creates a new cart in Emporix Commerce Engine. |
| [Get Cart](actions/get-cart.md) | GET | Retrieves a cart from Emporix Commerce Engine. |
| [List Cart Items](actions/list-cart-items.md) | GET | Retrieves items in a cart from Emporix Commerce Engine. |
| [List Carts](actions/list-carts.md) | GET | Retrieves carts from Emporix Commerce Engine. |
| [Search Carts](actions/search-carts.md) | GET | Finds carts in Emporix Commerce Engine by search criteria. |
| [Validate Cart](actions/validate-cart.md) | GET | Retrieves cart validation results from Emporix Commerce Engine. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Create Catalog](actions/create-catalog.md) | POST | Creates a new catalog in Emporix Commerce Engine. |
| [Get Catalog](actions/get-catalog.md) | GET | Retrieves a catalog from Emporix Commerce Engine. |
| [List Catalogs](actions/list-catalogs.md) | GET | Retrieves catalogs from Emporix Commerce Engine. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Emporix Commerce Engine. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Emporix Commerce Engine. |
| [List Category Trees](actions/list-category-trees.md) | GET | Retrieves category trees from Emporix Commerce Engine. |
| [Search Categories](actions/search-categories.md) | GET | Finds categories in Emporix Commerce Engine by search criteria. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Legal Entity](actions/get-legal-entity.md) | GET | Retrieves a legal entity from Emporix Commerce Engine. |
| [List Legal Entities](actions/list-legal-entities.md) | GET | Retrieves legal entities from Emporix Commerce Engine. |
| [Search Legal Entities](actions/search-legal-entities.md) | GET | Finds legal entities in Emporix Commerce Engine by search criteria. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [List Site Availability](actions/list-site-availability.md) | GET | Retrieves site availability from Emporix Commerce Engine. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Emporix Commerce Engine. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Emporix Commerce Engine. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Emporix Commerce Engine. |
| [List Order Transitions](actions/list-order-transitions.md) | GET | Retrieves sales order transitions from Emporix Commerce Engine. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Emporix Commerce Engine. |
| [Search Sales Orders](actions/search-sales-orders.md) | GET | Finds sales orders in Emporix Commerce Engine by search criteria. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates a sales order status in Emporix Commerce Engine. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Price](actions/get-price.md) | GET | Retrieves a price from Emporix Commerce Engine. |
| [Get Price List](actions/get-price-list.md) | GET | Retrieves a price list from Emporix Commerce Engine. |
| [List Price Lists](actions/list-price-lists.md) | GET | Retrieves price lists from Emporix Commerce Engine. |
| [List Prices](actions/list-prices.md) | GET | Retrieves prices from Emporix Commerce Engine. |
| [Match Prices](actions/match-prices.md) | GET | Finds matching prices in Emporix Commerce Engine. |
| [Search Prices](actions/search-prices.md) | GET | Finds prices in Emporix Commerce Engine by search criteria. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Emporix Commerce Engine. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Emporix Commerce Engine. |
| [List Product Templates](actions/list-product-templates.md) | GET | Retrieves product templates from Emporix Commerce Engine. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Emporix Commerce Engine. |
| [Patch Product](actions/patch-product.md) | PUT | Updates part of a product in Emporix Commerce Engine. |
| [Search Products](actions/search-products.md) | GET | Finds products in Emporix Commerce Engine by search criteria. |
| [Upsert Product](actions/upsert-product.md) | PUT | Updates a product in Emporix Commerce Engine, or creates it if missing. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | GET | Retrieves a brand from Emporix Commerce Engine. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Emporix Commerce Engine. |

