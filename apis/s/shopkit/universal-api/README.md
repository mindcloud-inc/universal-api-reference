# <img src="https://images.mindcloud.co/apps/icons/shopkit_1774629778632.png" alt="Shopkit logo" width="28" height="28"> Shopkit: Universal API

Manage store data, products, categories, brands, orders, clients, coupons, media, webhooks, and stats in Shopkit.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shopkit/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shopk.it/
- **Vendor API docs:** https://shopk.it/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Store](actions/get-store.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Create Brand](actions/create-brand.md) | POST | Creates a new brand in Shopkit. |
| [Delete Brand](actions/delete-brand.md) | DELETE | Deletes an existing brand from Shopkit. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Shopkit. |
| [Update Brand](actions/update-brand.md) | PUT | Updates an existing brand in Shopkit. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Shopkit. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from Shopkit. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Shopkit. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Shopkit. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Shopkit. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Shopkit. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Shopkit. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Shopkit. |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in Shopkit. |
| [Delete Coupon](actions/delete-coupon.md) | DELETE | Deletes an existing coupon from Shopkit. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves coupons from Shopkit. |
| [Update Coupon](actions/update-coupon.md) | PUT | Updates an existing coupon in Shopkit. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [List Media](actions/list-media.md) | GET | Retrieves media from Shopkit. |
| [Upload Media](actions/upload-media.md) | POST | Uploads media to Shopkit. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from Shopkit. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Shopkit. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Shopkit. |
| [Update Orders in Bulk](actions/update-orders-in-bulk.md) | PUT | Updates existing orders in bulk in Shopkit. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Shopkit. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Shopkit. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Shopkit. |
| [Search Products](actions/search-products.md) | GET | Finds products in Shopkit by search query. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Shopkit. |

### Product Option

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product Option](actions/delete-product-option.md) | DELETE | Deletes an existing product option from Shopkit. |
| [List Product Options](actions/list-product-options.md) | GET | Retrieves product options from Shopkit. |
| [Update Product Option](actions/update-product-option.md) | PUT | Updates an existing product option in Shopkit. |

### Product Option Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Option Group](actions/create-product-option-group.md) | POST | Creates a new product option group in Shopkit. |
| [Delete Product Option Group](actions/delete-product-option-group.md) | DELETE | Deletes an existing product option group from Shopkit. |
| [List Product Option Groups](actions/list-product-option-groups.md) | GET | Retrieves product option groups from Shopkit. |
| [Update Product Option Group](actions/update-product-option-group.md) | PUT | Updates an existing product option group in Shopkit. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Shopkit. |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats](actions/get-stats.md) | GET | Retrieves store statistics from Shopkit. |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store](actions/get-store.md) | GET | Retrieves store details from Shopkit. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Shopkit. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Shopkit. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Shopkit. |

