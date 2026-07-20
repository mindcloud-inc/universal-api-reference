# <img src="https://images.mindcloud.co/apps/icons/goodbarber-ecommerce_1773936348092.png" alt="Goodbarber eCommerce logo" width="28" height="28"> Goodbarber eCommerce: Universal API

Manage catalog, customers, orders, promotions, loyalty, push, and analytics for a GoodBarber Shopping app through the GoodBarber Commerce Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goodbarberECommerce/latest
- **Category:** Commerce
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.goodbarber.com/ecommerce/
- **Vendor API docs:** https://commerce.goodbarber.dev/publicapi/v2/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Front JWT](actions/validate-front-jwt.md) | GET |  |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET |  |
| [List Collections](actions/list-collections.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Invoice](actions/get-order-invoice.md) | GET |  |

### Loyalty Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get User Loyalty Points](actions/get-user-loyalty-points.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Product Paragraph

| Action | Method | Description |
| --- | --- | --- |
| [List Product Paragraphs](actions/list-product-paragraphs.md) | GET |  |

### Product Variant

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Variant](actions/get-product-variant.md) | GET |  |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Get Prospect](actions/get-prospect.md) | GET |  |
| [List Prospects](actions/list-prospects.md) | GET |  |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Shipping](actions/get-order-shipping.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Traffic Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Views Per Week Day](actions/get-page-views-per-week-day.md) | GET |  |
| [List App Downloads](actions/list-app-downloads.md) | GET |  |
| [List App Global Downloads](actions/list-app-global-downloads.md) | GET |  |
| [List App Launches](actions/list-app-launches.md) | GET |  |
| [List Page Views](actions/list-page-views.md) | GET |  |
| [List Session Times](actions/list-session-times.md) | GET |  |
| [List Unique App Launches](actions/list-unique-app-launches.md) | GET |  |

### Variant Option

| Action | Method | Description |
| --- | --- | --- |
| [Create Variant Option](actions/create-variant-option.md) | POST |  |
| [Delete Variant Option](actions/delete-variant-option.md) | DELETE |  |
| [List Variant Options](actions/list-variant-options.md) | GET |  |
| [Update Variant Option](actions/update-variant-option.md) | PUT |  |

