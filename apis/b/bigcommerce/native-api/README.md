# BigCommerce: Native API Reference

A consolidated summary of BigCommerce's API configuration and 65 documented operations.

- **API base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Store Hash:** `storeHash` · optional · Store ID used in requests

Send these headers with each API request:

```http
X-Auth-Token: <apiKey>
X-Bc-Store-Hash: <storeHash>
```

### OAuth 2.0

### Credentials

- **Store Hash:** `storeHash` · optional · Store ID used in requests

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.mindcloud.co/v1/oauth/bigcommerce/callback to approve access.
2. Exchange the returned authorization code with a POST request to https://login.bigcommerce.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `store_v2_orders store_v2_orders_read_only store_v2_transactions_read_only store_fulfillment_methods_read_only store_order_fulfillment_manage store_v2_products store_inventory_read_only store_locations store_v2_customers store_channel_settings store_channel_listings  store_b2b`.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `limit` in the query string to set the page size (default 50; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (65 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cart Item](actions/add-cart-item.md) | `POST /v3/carts/:cartId/items` | [docs](https://developer.bigcommerce.com/docs/rest-management/carts/items#add-cart-line-items) |
| [Create a Channel](actions/create-a-channel.md) | `POST /v3/channels` |  |
| [Create Customer](actions/create-customer.md) | `POST /v3/customers` |  |
| [Create Customer Address](actions/create-customer-address.md) | `POST /v3/customers/addresses` |  |
| [Create Product](actions/create-product.md) | `POST /v3/catalog/products` |  |
| [Create Product Image](actions/create-product-image.md) | `POST /v3/catalog/products/:productId/images` |  |
| [Create Product Metafield](actions/create-product-metafield.md) | `POST /v3/catalog/products/:productId/metafields` |  |
| [Create Product Modifier](actions/create-product-modifier.md) | `POST /v3/catalog/products/:productId/modifiers` |  |
| [Create Product Variant](actions/create-product-variant.md) | `POST /v3/catalog/products/:productId/variants` |  |
| [Create Product Variant Image](actions/create-product-variant-image.md) | `POST /v3/catalog/products/:productId/variants/:variantId/image` |  |
| [Create Product Variant Option](actions/create-product-variant-option.md) | `POST /v3/catalog/products/:productId/options` |  |
| [Create Products Channel Assignments](actions/create-products-channel-assignments.md) | `PUT /v3/catalog/products/channel-assignments` |  |
| [Create Refund](actions/create-refund.md) | `POST /v3/orders/:order_id/payment_actions/refunds` |  |
| [Create Refund Quote](actions/create-refund-quote.md) | `POST /v3/orders/:order_id/payment_actions/refund_quotes` |  |
| [Create Shipping For Order](actions/create-shipping-for-order.md) | `POST /v2/orders/:order_id/shipments` |  |
| [Create Webhook](actions/create-webhook.md) | `POST /v3/hooks` |  |
| [Delete Cart Item](actions/delete-cart-item.md) | `DELETE /v3/carts/:cartId/items/:itemId` | [docs](https://developer.bigcommerce.com/docs/rest-management/carts/items#delete-cart-line-item) |
| [Delete Product Image](actions/delete-product-image.md) | `DELETE /v3/catalog/products/:product_id/images/:image_id` |  |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v3/hooks/:webhookId` |  |
| [Get a Product](actions/get-a-product.md) | `GET /v3/catalog/products/:id` |  |
| [Get Accepted Payment Methods](actions/get-accepted-payment-methods.md) | `GET /v3/payments/methods` |  |
| [Get All Countries](actions/get-all-countries.md) | `GET /v2/countries` |  |
| [Get All Customers](actions/get-all-customers.md) | `GET /v3/customers` | [docs](https://developer.bigcommerce.com/docs/rest-management/customers#get-all-customers) |
| [Get All Customers (v2)](actions/get-all-customers-v2.md) | `GET /v2/customers` | [docs](https://developer.bigcommerce.com/docs/rest-management/customers#get-all-customers) |
| [Get All Product Images](actions/get-all-product-images.md) | `GET /v3/catalog/products/:product_id/images` |  |
| [Get All Product Variant Options](actions/get-all-product-variant-options.md) | `GET /v3/catalog/products/:productId/options` |  |
| [Get All Product Variants](actions/get-all-product-variants.md) | `GET /v3/catalog/products/:productId/variants` |  |
| [Get All Product Modifiers](actions/get-all-products-modifiers.md) | `GET /v3/catalog/products/:productId/modifiers` |  |
| [Get All States By Country](actions/get-all-states-by-country.md) | `GET /v2/countries/:countryId/states` |  |
| [Get Cart](actions/get-cart.md) | `GET /v3/carts/:cartID` |  |
| [Get Cart v2](actions/get-cart-v2.md) | `GET https://api.bigcommerce.com/stores/:storeHash/v3/carts/:cartId` |  |
| [Get Channel Currency](actions/get-channel-currency.md) | `GET /v3/channels/:channelId/currency-assignments` |  |
| [Get Channel Listings](actions/get-channel-listings.md) | `GET /v3/channels/:channelId/listings` |  |
| [Get Channels](actions/get-channels.md) | `GET /v3/channels` |  |
| [Get Checkout](actions/get-checkout.md) | `GET https://api.bigcommerce.com/stores/:storeHash/v3/checkouts/:checkoutId?include=:include` |  |
| [Get Companies](actions/get-companies.md) | `GET https://api-b2b.bigcommerce.com/api/v3/io/companies` | [docs](https://developer.bigcommerce.com/docs/rest-management/customers#get-all-customers) |
| [Get Order Coupons](actions/get-order-coupons.md) | `GET /v2/orders/:orderID/coupons` | [docs](https://developer.bigcommerce.com/docs/rest-management/orders/order-coupons#list-order-coupons) |
| [Get Order Custom Fields](actions/get-order-custom-fields.md) | `GET /v3/orders/:orderId/custom-fields` |  |
| [Get Order Shipping Addresses](actions/get-order-shipping-addresses.md) | `GET /v2/orders/:orderId/shipping_addresses` |  |
| [Get Order Statuses](actions/get-order-statuses.md) | `GET /v2/order_statuses` |  |
| [Get Orders](actions/get-orders.md) | `GET /v2/orders` | [docs](https://developer.bigcommerce.com/docs/rest-management/orders#get-all-orders) |
| [Get Product Channel Assignments](actions/get-product-channel-assignments.md) | `GET /v3/catalog/products/channel-assignments` |  |
| [Get Product Metafield](actions/get-product-metafield.md) | `GET /v3/catalog/products/:productId/metafields/:metafieldId` |  |
| [Get Product Metafields](actions/get-product-metafields.md) | `GET /v3/catalog/products/:productId/metafields` |  |
| [Get Products](actions/get-products.md) | `GET /v3/catalog/products` |  |
| [Get Products In Order](actions/get-products-in-order.md) | `GET /v2/orders/:orderId/products` |  |
| [Get Shipment from Order](actions/get-shipment-from-order.md) | `GET /v2/orders/:orderId/shipments` |  |
| [Get Shipping Method](actions/get-shipping-methods.md) | `GET /v2/shipping/zones/:zoneID/methods/:methodID` |  |
| [Get Sites](actions/get-sites.md) | `GET /v3/sites` |  |
| [Get Store Information](actions/get-store-information.md) | `GET /v3/sites` |  |
| [Get Webhooks](actions/get-webhooks.md) | `GET /v3/hooks` |  |
| [Get Webhooks Admin Info](actions/get-webhooks-admin-info.md) | `GET /v3/hooks/admin` | [docs](https://developer.bigcommerce.com/docs/webhooks/webhooks/webhooks-admin#get-admin-info) |
| [List Customer Addresses](actions/list-customer-addresses.md) | `GET /v3/customers/addresses` |  |
| [List Order Transactions](actions/list-order-transactions.md) | `GET /v3/orders/:orderId/transactions` |  |
| [Update Checkout](actions/update-checkout.md) | `PUT /v3/checkouts/:cartID` |  |
| [Update Customer](actions/update-customer.md) | `PUT /v3/customers` |  |
| [Update Customer Address](actions/update-customer-address.md) | `PUT /v3/customers/addresses` |  |
| [Update Order](actions/update-order.md) | `PUT /v2/orders/:orderId` |  |
| [Update Product](actions/update-product.md) | `PUT /v3/catalog/products/:productId` |  |
| [Update Product Image](actions/update-product-image.md) | `PUT /v3/catalog/products/:productId/images/:imageId` |  |
| [Update Product Metafield](actions/update-product-metafield.md) | `PUT /v3/catalog/products/:productId/metafields/:metafieldId` |  |
| [Update Product Variant](actions/update-product-variant.md) | `PUT /v3/catalog/products/:productId/variants/:variantId` |  |
| [Update Product Variant Option](actions/update-product-variant-option.md) | `PUT /v3/catalog/products/:productId/options/:optionId` |  |
| [Update Shipping for Order](actions/update-shipping-for-order.md) | `PUT /v2/orders/:orderId/shipments/:shipmentId` |  |
| [Update Webhook](actions/update-webhook.md) | `PUT /v3/hooks/:webhookId` |  |
