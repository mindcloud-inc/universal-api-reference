# <img src="https://images.mindcloud.co/apps/icons/bigcom_1782232860205.png" alt="BigCommerce logo" width="28" height="28"> BigCommerce: Universal API

Enterprise eCommerce, simplified.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigcommerce/latest
- **Actions:** 65
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Orders](actions/get-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (65)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create a Channel](actions/create-a-channel.md) | POST |  |
| [Get Channel Currency](actions/get-channel-currency.md) | GET |  |
| [Get Channel Listings](actions/get-channel-listings.md) | GET |  |
| [Get Channels](actions/get-channels.md) | GET |  |
| [Get Sites](actions/get-sites.md) | GET |  |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Add Cart Item](actions/add-cart-item.md) | POST |  |
| [Delete Cart Item](actions/delete-cart-item.md) | DELETE |  |
| [Get Cart](actions/get-cart.md) | GET |  |
| [Get Cart v2](actions/get-cart-v2.md) | GET |  |
| [Get Checkout](actions/get-checkout.md) | GET |  |
| [Update Checkout](actions/update-checkout.md) | PUT |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get All Customers](actions/get-all-customers.md) | GET |  |
| [Get All Customers (v2)](actions/get-all-customers-v2.md) | GET |  |
| [Get Companies](actions/get-companies.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Create Customer Address](actions/create-customer-address.md) | POST |  |
| [List Customer Addresses](actions/list-customer-addresses.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |
| [Update Customer Address](actions/update-customer-address.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST |  |
| [Create Refund Quote](actions/create-refund-quote.md) | POST |  |

### Metafield

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Metafield](actions/create-product-metafield.md) | POST |  |
| [Update Product Metafield](actions/update-product-metafield.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Coupons](actions/get-order-coupons.md) | GET | Lists all order coupons. Optional parameters can be passed in. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Accepted Payment Methods](actions/get-accepted-payment-methods.md) | GET |  |

### Product Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Image](actions/create-product-image.md) | POST |  |
| [Update Product Image](actions/update-product-image.md) | PUT |  |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Modifier](actions/create-product-modifier.md) | POST |  |
| [Create Product Variant](actions/create-product-variant.md) | POST |  |
| [Create Product Variant Image](actions/create-product-variant-image.md) | POST |  |
| [Create Product Variant Option](actions/create-product-variant-option.md) | POST |  |
| [Get All Product Variant Options](actions/get-all-product-variant-options.md) | GET |  |
| [Get All Product Variants](actions/get-all-product-variants.md) | GET |  |
| [Get All Product Modifiers](actions/get-all-products-modifiers.md) | GET |  |
| [Get Product Metafield](actions/get-product-metafield.md) | GET |  |
| [Get Product Metafields](actions/get-product-metafields.md) | GET |  |
| [Update Product Variant](actions/update-product-variant.md) | PUT |  |
| [Update Product Variant Option](actions/update-product-variant-option.md) | PUT |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Create Products Channel Assignments](actions/create-products-channel-assignments.md) | PUT |  |
| [Delete Product Image](actions/delete-product-image.md) | DELETE |  |
| [Get a Product](actions/get-a-product.md) | GET |  |
| [Get All Product Images](actions/get-all-product-images.md) | GET |  |
| [Get Product Channel Assignments](actions/get-product-channel-assignments.md) | GET |  |
| [Get Products](actions/get-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipping For Order](actions/create-shipping-for-order.md) | POST |  |
| [Get Order Custom Fields](actions/get-order-custom-fields.md) | GET | Gets the order by the ID |
| [Get Order Shipping Addresses](actions/get-order-shipping-addresses.md) | GET | Gets the shipping addresses in an order |
| [Get Orders](actions/get-orders.md) | GET | Gets all orders |
| [Get Products In Order](actions/get-products-in-order.md) | GET | Gets the products listed in the order |
| [Get Shipment from Order](actions/get-shipment-from-order.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT | Updates an Order |
| [Update Shipping for Order](actions/update-shipping-for-order.md) | PUT |  |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get All Countries](actions/get-all-countries.md) | GET |  |
| [Get All States By Country](actions/get-all-states-by-country.md) | GET |  |
| [Get Order Statuses](actions/get-order-statuses.md) | GET |  |
| [Get Shipping Method](actions/get-shipping-methods.md) | GET |  |

### Store

| Action | Method | Description |
| --- | --- | --- |
| [Get Store Information](actions/get-store-information.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Order Transactions](actions/list-order-transactions.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhooks](actions/get-webhooks.md) | GET |  |
| [Get Webhooks Admin Info](actions/get-webhooks-admin-info.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

