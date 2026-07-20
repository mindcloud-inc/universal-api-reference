# <img src="https://images.mindcloud.co/apps/icons/booqable_1773271901625.png" alt="Booqable logo" width="28" height="28"> Booqable: Universal API

Manage rental inventory, orders, customers, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/booqable/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://booqable.com
- **Vendor API docs:** https://developers.booqable.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Items](actions/list-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Availability](actions/get-product-availability.md) | GET | Retrieves availability for a product in Booqable. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Booqable. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Booqable. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer records from Booqable. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Booqable by search criteria. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Booqable. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from Booqable. |
| [List Items](actions/list-items.md) | GET | Retrieves item records from Booqable. |
| [Search Items](actions/search-items.md) | GET | Finds items in Booqable by search criteria. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Booqable. |
| [Get New Order](actions/get-new-order.md) | GET | Retrieves an existing or new order for the current employee in Booqable. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Booqable. |
| [List Orders](actions/list-orders.md) | GET | Retrieves order records from Booqable. |
| [Search Orders](actions/search-orders.md) | GET | Finds orders in Booqable by search criteria. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Booqable. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Booqable. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Booqable. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Booqable. |
| [Search Products](actions/search-products.md) | GET | Finds products in Booqable by search criteria. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Booqable. |

### Stock Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Item](actions/get-stock-item.md) | GET | Retrieves a stock item from Booqable. |
| [List Stock Items](actions/list-stock-items.md) | GET | Retrieves stock item records from Booqable. |
| [Update Stock Item](actions/update-stock-item.md) | PUT | Updates an existing stock item in Booqable. |

