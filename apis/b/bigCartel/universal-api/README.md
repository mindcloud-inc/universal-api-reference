# <img src="https://images.mindcloud.co/apps/icons/images-12_1775826994367.png" alt="Big Cartel logo" width="28" height="28"> Big Cartel: Universal API

Manage Big Cartel products, orders, discounts, pages, and shipments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigCartel/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bigcartel.com/
- **Vendor API docs:** https://developers.bigcartel.com/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Get Abandoned Cart](actions/get-abandoned-cart.md) | GET | Retrieves an abandoned cart from Big Cartel. |
| [Get All Abandoned Carts](actions/get-all-abandoned-carts.md) | GET | Retrieves abandoned carts from Big Cartel. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a category in Big Cartel. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes a category from Big Cartel. |
| [Get All Categories](actions/get-all-categories.md) | GET | Retrieves categories from Big Cartel. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Big Cartel. |
| [Reposition Categories](actions/reposition-categories.md) | PUT | Updates category positions in Big Cartel. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Big Cartel. |

### Discounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Discount](actions/create-discount.md) | POST | Creates a discount in Big Cartel. |
| [Delete Discount](actions/delete-discount.md) | DELETE | Deletes a discount from Big Cartel. |
| [Get All Discounts](actions/get-all-discounts.md) | GET | Retrieves discounts from Big Cartel. |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a discount from Big Cartel. |
| [Update Discount](actions/update-discount.md) | PUT | Updates an existing discount in Big Cartel. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get All Orders](actions/get-all-orders.md) | GET | Retrieves orders from Big Cartel. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Big Cartel. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Big Cartel. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Big Cartel. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a page in Big Cartel. |
| [Get All Pages](actions/get-all-pages.md) | GET | Retrieves pages from Big Cartel. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Big Cartel. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Big Cartel. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get All Products](actions/get-all-products.md) | GET | Retrieves products from Big Cartel. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Big Cartel. |
| [Reposition Products](actions/reposition-products.md) | PUT | Updates product positions in Big Cartel. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Big Cartel. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a shipment for a Big Cartel order. |
| [Delete Shipment](actions/delete-shipment.md) | DELETE | Deletes a shipment from a Big Cartel order. |
| [Get All Shipments](actions/get-all-shipments.md) | GET | Retrieves shipments from a Big Cartel order. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from a Big Cartel order. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates a shipment for a Big Cartel order. |

