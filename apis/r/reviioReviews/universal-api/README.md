# <img src="https://images.mindcloud.co/apps/icons/reviio-reviews_1776968073800.png" alt="Revi.io Reviews logo" width="28" height="28"> Revi.io Reviews: Universal API

Revi.io API wrapper for syncing ecommerce orders and products, linking order line items, and retrieving shop and review data from Revi.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reviioReviews/latest
- **Category:** Support / Customer Success
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://revi.io
- **Vendor API docs:** https://docs.revi7.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Hello World](actions/hello-world.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world?connectionId=$CONNECTION_ID&test=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Connection Test

| Action | Method | Description |
| --- | --- | --- |
| [Hello World](actions/hello-world.md) | GET | Tests the Revi.io Reviews API connection. |

### Order Deletion

| Action | Method | Description |
| --- | --- | --- |
| [Delete Orders](actions/delete-orders.md) | DELETE | Deletes orders from Revi.io Reviews. |

### Order Product Full Link

| Action | Method | Description |
| --- | --- | --- |
| [Link Full Products to Orders](actions/link-full-products-to-orders.md) | PUT | Links full products to orders in Revi.io Reviews. |

### Order Product Link

| Action | Method | Description |
| --- | --- | --- |
| [Link Products to Orders](actions/link-products-to-orders.md) | PUT | Links products to orders in Revi.io Reviews. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Order Statuses](actions/update-order-statuses.md) | PUT | Updates order statuses in Revi.io Reviews. |

### Order Sync

| Action | Method | Description |
| --- | --- | --- |
| [Create Orders](actions/create-orders.md) | POST | Creates orders in Revi.io Reviews. |

### Product Review Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Review Info](actions/get-product-review-info.md) | GET | Retrieves product review info from Revi.io Reviews. |

### Product Sync

| Action | Method | Description |
| --- | --- | --- |
| [Create Products](actions/create-products.md) | POST | Creates products in Revi.io Reviews. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Reviews](actions/get-reviews.md) | GET | Retrieves reviews from Revi.io Reviews. |

### Shop Rating

| Action | Method | Description |
| --- | --- | --- |
| [Get Shop Rating Info](actions/get-shop-rating-info.md) | GET | Retrieves shop rating info from Revi.io Reviews. |

