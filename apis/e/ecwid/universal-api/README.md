# <img src="https://images.mindcloud.co/apps/icons/ecwid_1773256323165.png" alt="Ecwid logo" width="28" height="28"> Ecwid: Universal API

Manage Ecwid products, orders, customers, and store data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ecwid/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ecwid.com/
- **Vendor API docs:** https://docs.ecwid.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Store Profile](actions/get-store-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-store-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Search Product Brands](actions/search-product-brands.md) | GET | Finds product brands in Ecwid. |

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Get Abandoned Cart](actions/get-abandoned-cart.md) | GET | Retrieves an abandoned cart from Ecwid. |
| [Search Abandoned Carts](actions/search-abandoned-carts.md) | GET | Finds abandoned carts in Ecwid. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Ecwid. |
| [Search Categories](actions/search-categories.md) | GET | Finds categories in Ecwid. |
| [Search Categories by Path](actions/search-categories-by-path.md) | GET | Finds categories in Ecwid by path. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Search Discount Coupons](actions/search-discount-coupons.md) | GET | Finds discount coupons in Ecwid. |

### Customergroup

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Group](actions/get-customer-group.md) | GET | Retrieves a customer group from Ecwid. |
| [Search Customer Groups](actions/search-customer-groups.md) | GET | Finds customer groups in Ecwid. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Ecwid. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in Ecwid. |

### Inventorylevel

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Product Stock](actions/adjust-product-stock.md) | PUT | Updates product stock in Ecwid. |

### Orderextrafield

| Action | Method | Description |
| --- | --- | --- |
| [Search Order Extra Fields](actions/search-order-extra-fields.md) | GET | Finds order extra fields in Ecwid. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Order](actions/get-last-order.md) | GET | Retrieves the last order from Ecwid. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Ecwid. |
| [Search Orders](actions/search-orders.md) | GET | Finds orders in Ecwid. |

### Orderstatus

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Status](actions/get-order-status.md) | GET | Retrieves an order status from Ecwid. |
| [Search Order Statuses](actions/search-order-statuses.md) | GET | Finds order statuses in Ecwid. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Search Products](actions/search-products.md) | GET | Finds products in Ecwid. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Ecwid. |

### Productswatch

| Action | Method | Description |
| --- | --- | --- |
| [Get Recently Used Product Swatches](actions/get-recently-used-product-swatches.md) | GET | Retrieves recently used product swatches from Ecwid. |

### Repeatorderurl

| Action | Method | Description |
| --- | --- | --- |
| [Get Repeat Order URL](actions/get-repeat-order-url.md) | GET | Retrieves a repeat order URL from Ecwid. |

### Shippingoption

| Action | Method | Description |
| --- | --- | --- |
| [Search Shipping Options](actions/search-shipping-options.md) | GET | Finds shipping options in Ecwid. |

### Storeprofile

| Action | Method | Description |
| --- | --- | --- |
| [Get Store Profile](actions/get-store-profile.md) | GET | Retrieves a store profile from Ecwid. |

