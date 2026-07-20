# <img src="https://images.mindcloud.co/apps/icons/keysender-icon-square_1775674815946.png" alt="Keysender logo" width="28" height="28"> Keysender: Universal API

Keysender is a digital product fulfillment platform API for catalog browsing, order reservation, order creation, customer management, and code/database operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keysender/latest
- **Category:** Commerce
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.keysender.com
- **Vendor API docs:** https://panel.keysender.co.uk/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Keysender. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Keysender. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Keysender. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Keysender. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a database in Keysender. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes an existing database from Keysender. |
| [Get Database](actions/get-database.md) | GET | Retrieves a database from Keysender. |
| [Get Databases](actions/get-databases.md) | GET | Retrieves databases from Keysender. |
| [Update Database](actions/update-database.md) | PUT | Updates an existing database in Keysender. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Delete Code](actions/delete-code.md) | DELETE | Deletes an existing code from Keysender. |
| [Get Codes](actions/get-codes.md) | GET | Retrieves codes from Keysender. |
| [Update Code](actions/update-code.md) | PUT | Updates an existing code in Keysender. |
| [Upload Text Codes](actions/upload-text-codes.md) | POST | Uploads text codes to Keysender. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order Item](actions/cancel-order-item.md) | PUT | Cancels an order item in Keysender. |
| [Create Order From Reservation](actions/create-order-from-reservation.md) | POST | Creates an order from a Keysender reservation. |
| [Get Order Details](actions/get-order-details.md) | GET | Retrieves order details from Keysender. |
| [Reserve Catalog Items](actions/reserve-catalog-items.md) | POST | Creates a catalog reservation in Keysender. |
| [Top Up Order Item](actions/top-up-order-item.md) | POST | Creates a top-up for a Keysender order item. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Transaction](actions/add-custom-transaction.md) | POST | Creates a custom transaction in Keysender. |
| [Add Transaction From Source](actions/add-transaction-from-source.md) | POST | Creates a transaction from a source in Keysender. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product By SKU](actions/get-product-by-sku.md) | GET | Retrieves a product from Keysender by SKU. |
| [List Discounted Products](actions/list-discounted-products.md) | GET | Retrieves discounted products from Keysender. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Keysender. |
| [List Products By Category](actions/list-products-by-category.md) | GET | Retrieves products from Keysender in a category. |
| [List Products By Category And Region](actions/list-products-by-category-and-region.md) | GET | Retrieves products from Keysender for a category and region. |
| [List Products By Language](actions/list-products-by-language.md) | GET | Retrieves products from Keysender for a language. |
| [List Products By Maximum Price](actions/list-products-by-maximum-price.md) | GET | Retrieves products from Keysender below a maximum price. |
| [List Products By Minimum Price](actions/list-products-by-minimum-price.md) | GET | Retrieves products from Keysender above a minimum price. |
| [List Products By Minimum Quantity](actions/list-products-by-minimum-quantity.md) | GET | Retrieves products from Keysender above a minimum quantity. |
| [List Products By Price Range](actions/list-products-by-price-range.md) | GET | Retrieves products from Keysender within a price range. |
| [List Products By Region](actions/list-products-by-region.md) | GET | Retrieves products from Keysender for a region. |
| [List Products By Region And Language](actions/list-products-by-region-and-language.md) | GET | Retrieves products from Keysender for a region and language. |
| [List Products By Type](actions/list-products-by-type.md) | GET | Retrieves products from Keysender by type. |
| [List Products For Bulk Fulfillment](actions/list-products-for-bulk-fulfillment.md) | GET | Retrieves products from Keysender for bulk fulfillment. |
| [List Products Sorted By Price Descending](actions/list-products-sorted-by-price-descending.md) | GET | Retrieves products from Keysender sorted by descending price. |
| [List Products Updated Since](actions/list-products-updated-since.md) | GET | Retrieves products updated since a date from Keysender. |
| [List Products With Additional Information](actions/list-products-with-additional-information.md) | GET | Retrieves products with additional information from Keysender. |
| [Search Products By Name](actions/search-products-by-name.md) | GET | Finds products in Keysender by name. |
| [Search Products By SKU](actions/search-products-by-sku.md) | GET | Finds products in Keysender by SKU. |

