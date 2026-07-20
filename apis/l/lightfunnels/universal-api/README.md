# <img src="https://images.mindcloud.co/apps/icons/lightfunnels-icon-512_1776451232416.png" alt="Lightfunnels logo" width="28" height="28"> Lightfunnels: Universal API

OAuth2 GraphQL API for Lightfunnels funnels, products, orders, customers, discounts, reviews, segments, stores, settings, bundles, collections, shipping rate groups, and app charges.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightfunnels/latest
- **Category:** Commerce
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lightfunnels.com
- **Vendor API docs:** https://developer.lightfunnels.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account Pixels](actions/retrieve-account-pixels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### Account.integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Facebook Conversion API Integration](actions/create-facebook-conversion-api-integration.md) | POST |  |
| [Remove Integration](actions/remove-integration.md) | DELETE |  |
| [Retrieve Integrations](actions/retrieve-integrations.md) | GET |  |

### Account.settings

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account Pixels](actions/retrieve-account-pixels.md) | GET |  |
| [Update Account Pixels](actions/update-account-pixels.md) | PUT |  |

### Account.webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |

### Commerce.appcharge

| Action | Method | Description |
| --- | --- | --- |
| [Create App Charge](actions/create-app-charge.md) | POST |  |
| [Get App Charge](actions/get-app-charge.md) | GET |  |
| [List App Charges](actions/list-app-charges.md) | GET |  |

### Commerce.bundle

| Action | Method | Description |
| --- | --- | --- |
| [Create Bundle](actions/create-bundle.md) | POST |  |
| [Delete Bundle](actions/delete-bundle.md) | DELETE |  |
| [Get Bundle](actions/get-bundle.md) | GET |  |
| [List Bundles](actions/list-bundles.md) | GET |  |
| [Update Bundle](actions/update-bundle.md) | PUT |  |

### Commerce.discount

| Action | Method | Description |
| --- | --- | --- |
| [Create Discount](actions/create-discount.md) | POST |  |
| [Delete Discount](actions/delete-discount.md) | DELETE |  |
| [Get Discount](actions/get-discount.md) | GET |  |
| [List Discounts](actions/list-discounts.md) | GET |  |
| [Update Discount](actions/update-discount.md) | PUT |  |

### Commerce.funnel

| Action | Method | Description |
| --- | --- | --- |
| [Create Funnel](actions/create-funnel.md) | POST |  |
| [Delete Funnel](actions/delete-funnel.md) | DELETE |  |
| [Get Funnel](actions/get-funnel.md) | GET |  |
| [List Funnels](actions/list-funnels.md) | GET |  |
| [Update Funnel](actions/update-funnel.md) | PUT |  |

### Commerce.order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | DELETE |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |

### Commerce.product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Products](actions/delete-products.md) | DELETE |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Commerce.review

| Action | Method | Description |
| --- | --- | --- |
| [Create Review](actions/create-review.md) | POST |  |
| [Delete Review](actions/delete-review.md) | DELETE |  |
| [Get Review](actions/get-review.md) | GET |  |
| [List Reviews](actions/list-reviews.md) | GET |  |
| [Update Review](actions/update-review.md) | PUT |  |

### Commerce.shippingrategroup

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipping Rate Group](actions/create-shipping-rate-group.md) | POST |  |
| [Delete Shipping Rate Group](actions/delete-shipping-rate-group.md) | DELETE |  |
| [List Shipping Rate Groups](actions/list-shipping-rate-groups.md) | GET |  |
| [Update Shipping Rate Group](actions/update-shipping-rate-group.md) | PUT |  |

### Commerce.store

| Action | Method | Description |
| --- | --- | --- |
| [Add Products to Store](actions/add-products-to-store.md) | PUT |  |
| [Create Store](actions/create-store.md) | POST |  |
| [Delete Store](actions/delete-store.md) | DELETE |  |
| [Get Store](actions/get-store.md) | GET |  |
| [List Stores](actions/list-stores.md) | GET |  |
| [Update Store](actions/update-store.md) | PUT |  |

### Content.collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST |  |
| [Delete Collection](actions/delete-collection.md) | DELETE |  |
| [Get Collection](actions/get-collection.md) | GET |  |
| [List Collections](actions/list-collections.md) | GET |  |
| [Update Collection](actions/update-collection.md) | PUT |  |

### Crm.customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Crm.segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Delete Segment](actions/delete-segment.md) | DELETE |  |
| [Get Segment](actions/get-segment.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |
| [Update Segment](actions/update-segment.md) | PUT |  |

