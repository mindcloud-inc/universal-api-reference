# <img src="https://images.mindcloud.co/apps/icons/you-can_1776695993560.png" alt="YouCan logo" width="28" height="28"> YouCan: Universal API

YouCan store admin integration for products, orders, customers, coupons, and pages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/youCan/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://youcan.shop
- **Vendor API docs:** https://developer.youcan.shop/store-admin/introduction/oauth

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in YouCan. |
| [Delete Coupon](actions/delete-coupon.md) | DELETE | Deletes an existing coupon from YouCan. |
| [Get Coupon](actions/get-coupon.md) | GET | Retrieves details for a coupon from YouCan. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves a list of coupons from YouCan. |
| [Update Coupon](actions/update-coupon.md) | PUT | Updates an existing coupon in YouCan. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in YouCan. |
| [Create Customer Address](actions/create-customer-address.md) | POST | Creates a customer address in YouCan. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from YouCan. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves details for a customer from YouCan. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from YouCan. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in YouCan. |
| [Update Customer Address](actions/update-customer-address.md) | PUT | Updates an existing customer address in YouCan. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Close Order](actions/close-order.md) | PUT | Updates an order in YouCan by closing it. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in YouCan. |
| [Fulfill Order](actions/fulfill-order.md) | PUT | Updates an order in YouCan by fulfilling it. |
| [Get Order](actions/get-order.md) | GET | Retrieves details for an order from YouCan. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from YouCan. |
| [Mark Order As Paid](actions/mark-order-as-paid.md) | PUT | Updates an order in YouCan by marking it paid. |
| [Order Statuses](actions/order-statuses.md) | GET | Retrieves custom order statuses from YouCan. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates an order status in YouCan. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in YouCan. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from YouCan. |
| [Get Page](actions/get-page.md) | GET | Retrieves details for a page from YouCan. |
| [List Pages](actions/list-pages.md) | GET | Retrieves a list of pages from YouCan. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in YouCan. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in YouCan. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from YouCan. |
| [Get Product](actions/get-product.md) | GET | Retrieves details for a product from YouCan. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from YouCan. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in YouCan. |

