# Gelato: Native API Reference

A consolidated summary of Gelato's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.gelato.com/docs/
- **API base URL:** `https://order.gelatoapis.com`

## Authentication

### API Key

Gelato API key auth. Use the secret as the X-API-KEY request header. Test connection provisioning is blocked until an admin API key is available.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://dashboard.gelato.com/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Order v2](actions/cancel-order-v2.md) | `POST https://api.gelato.com/v2/order/cancel` | [docs](https://dashboard.gelato.com/docs/orders/v2/cancel/) |
| [Cancel Order v3](actions/cancel-order-v3.md) | `POST /v3/orders/{{orderId}}:cancel` | [docs](https://dashboard.gelato.com/docs/orders/v3/cancel/) |
| [Cancel Order v4](actions/cancel-order-v4.md) | `POST /v4/orders/{{orderId}}:cancel` | [docs](https://dashboard.gelato.com/docs/orders/v4/cancel/) |
| [Cover Dimensions](actions/cover-dimensions.md) | `GET https://product.gelatoapis.com/v3/products/{{productUid}}/cover-dimensions` | [docs](https://dashboard.gelato.com/docs/products/product/cover-dimensions/) |
| [Create Order v2](actions/create-order-v2.md) | `POST https://api.gelato.com/v2/order/create` | [docs](https://dashboard.gelato.com/docs/orders/v2/create/) |
| [Create Order v3](actions/create-order-v3.md) | `POST /v3/orders` | [docs](https://dashboard.gelato.com/docs/orders/v3/create/) |
| [Create Order v4](actions/create-order-v4.md) | `POST /v4/orders` | [docs](https://dashboard.gelato.com/docs/orders/v4/create/) |
| [Delete Draft Order v3](actions/delete-draft-order-v3.md) | `DELETE /v3/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v3/delete/) |
| [Delete Draft Order v4](actions/delete-draft-order-v4.md) | `DELETE /v4/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v4/delete/) |
| [Get Catalog](actions/get-catalog.md) | `GET https://product.gelatoapis.com/v3/catalogs/{{catalogUid}}` | [docs](https://dashboard.gelato.com/docs/products/catalog/get/) |
| [Get Order Status v2](actions/get-order-status-v2.md) | `GET https://api.gelato.com/v2/order/status/{{orderReferenceId}}` | [docs](https://dashboard.gelato.com/docs/orders/v2/status/) |
| [Get Order v3](actions/get-order-v3.md) | `GET /v3/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v3/get/) |
| [Get Order v4](actions/get-order-v4.md) | `GET /v4/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v4/get/) |
| [Get Product](actions/get-product.md) | `GET https://product.gelatoapis.com/v3/products/{{productUid}}` | [docs](https://dashboard.gelato.com/docs/products/product/get/) |
| [Get Shipping Address v2](actions/get-shipping-address-v2.md) | `GET https://api.gelato.com/v2/order/{{orderReferenceId}}/address` | [docs](https://dashboard.gelato.com/docs/orders/v2/shipping-address-get/) |
| [Get Shipping Address v3](actions/get-shipping-address-v3.md) | `GET /v3/orders/{{orderId}}/shipping-address` | [docs](https://dashboard.gelato.com/docs/orders/v3/shipping-address-get/) |
| [List Catalogs](actions/list-catalogs.md) | `GET https://product.gelatoapis.com/v3/catalogs` | [docs](https://dashboard.gelato.com/docs/products/catalog/list/) |
| [Patch Draft Order v3](actions/patch-draft-order-v3.md) | `PATCH /v3/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v3/patch/) |
| [Patch Draft Order v4](actions/patch-draft-order-v4.md) | `PATCH /v4/orders/{{orderId}}` | [docs](https://dashboard.gelato.com/docs/orders/v4/patch/) |
| [Price](actions/price.md) | `GET https://product.gelatoapis.com/v3/products/{{productUid}}/prices` | [docs](https://dashboard.gelato.com/docs/products/prices/) |
| [Quote Order v2](actions/quote-order-v2.md) | `POST https://api.gelato.com/v2/quote` | [docs](https://dashboard.gelato.com/docs/orders/v2/quote/) |
| [Quote Order v3](actions/quote-order-v3.md) | `POST /v3/orders:quote` | [docs](https://dashboard.gelato.com/docs/orders/v3/quote/) |
| [Quote Order v4](actions/quote-order-v4.md) | `POST /v4/orders:quote` | [docs](https://dashboard.gelato.com/docs/orders/v4/quote/) |
| [Search Orders v3](actions/search-orders-v3.md) | `POST /v3/orders:search` | [docs](https://dashboard.gelato.com/docs/orders/v3/search/) |
| [Search Orders v4](actions/search-orders-v4.md) | `POST /v4/orders:search` | [docs](https://dashboard.gelato.com/docs/orders/v4/search/) |
| [Search Products](actions/search-products.md) | `POST https://product.gelatoapis.com/v3/catalogs/{{catalogUid}}/products:search` | [docs](https://dashboard.gelato.com/docs/products/product/search/) |
| [Shipment Methods](actions/shipment-methods.md) | `GET https://shipment.gelatoapis.com/v1/shipment-methods` | [docs](https://dashboard.gelato.com/docs/shipment/methods/) |
| [Stock Availability](actions/stock-availability.md) | `POST https://product.gelatoapis.com/v3/stock/region-availability` | [docs](https://dashboard.gelato.com/docs/products/stock/region-availability/) |
| [Update Shipping Address v2](actions/update-shipping-address-v2.md) | `PUT https://api.gelato.com/v2/order/{{orderReferenceId}}/address` | [docs](https://dashboard.gelato.com/docs/orders/v2/shipping-address-update/) |
| [Update Shipping Address v3](actions/update-shipping-address-v3.md) | `PUT /v3/orders/{{orderId}}/shipping-address` | [docs](https://dashboard.gelato.com/docs/orders/v3/shipping-address-update/) |
