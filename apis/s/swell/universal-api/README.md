# <img src="https://images.mindcloud.co/apps/icons/swell_1775845634752.png" alt="Swell logo" width="28" height="28"> Swell: Universal API

Manage products, orders, customers, subscriptions, and promotions in Swell

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swell/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.swell.is
- **Vendor API docs:** https://developers.swell.is/backend-api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Delete Account](actions/delete-account.md) | DELETE |  |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Cart

| Action | Method | Description |
| --- | --- | --- |
| [Create Cart](actions/create-cart.md) | POST |  |
| [Delete Cart](actions/delete-cart.md) | DELETE |  |
| [Get Cart](actions/get-cart.md) | GET |  |
| [List Carts](actions/list-carts.md) | GET |  |
| [Update Cart](actions/update-cart.md) | PUT |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Delete Category](actions/delete-category.md) | DELETE |  |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST |  |
| [Delete Coupon](actions/delete-coupon.md) | DELETE |  |
| [Get Coupon](actions/get-coupon.md) | GET |  |
| [List Coupons](actions/list-coupons.md) | GET |  |
| [Update Coupon](actions/update-coupon.md) | PUT |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Delete Order](actions/delete-order.md) | DELETE |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Promotion

| Action | Method | Description |
| --- | --- | --- |
| [Create Promotion](actions/create-promotion.md) | POST |  |
| [Delete Promotion](actions/delete-promotion.md) | DELETE |  |
| [Get Promotion](actions/get-promotion.md) | GET |  |
| [List Promotions](actions/list-promotions.md) | GET |  |
| [Update Promotion](actions/update-promotion.md) | PUT |  |

### Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create Variant](actions/create-variant.md) | POST |  |
| [Delete Variant](actions/delete-variant.md) | DELETE |  |
| [Get Variant](actions/get-variant.md) | GET |  |
| [List Variants](actions/list-variants.md) | GET |  |
| [Update Variant](actions/update-variant.md) | PUT |  |

