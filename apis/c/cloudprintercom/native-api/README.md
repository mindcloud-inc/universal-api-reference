# Cloudprinter.com: Native API Reference

A consolidated summary of Cloudprinter.com's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0
- **API base URL:** `https://api.cloudprinter.com`

## Authentication

### API Key

Use a Cloudprinter API key from Development > API interfaces.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://knowledge.cloudprinter.com/print_api_where_can_i_find_change_the_api_key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Order](actions/add-order.md) | `POST /cloudcore/1.0/orders/add` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#add-order) |
| [Cancel Order](actions/cancel-order.md) | `POST /cloudcore/1.0/orders/cancel` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#cancel-order) |
| [Get Order Info](actions/get-order-info.md) | `POST /cloudcore/1.0/orders/info` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#get-order-info) |
| [Get Order Log](actions/get-order-log.md) | `POST /cloudcore/1.0/orders/log` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#order-log) |
| [Get Order Quote](actions/get-order-quote.md) | `POST /cloudcore/1.0/orders/quote` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#order-quote) |
| [Get Product Info](actions/get-product-info.md) | `POST /cloudcore/1.0/products/info` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#product-info) |
| [List Orders](actions/list-orders.md) | `POST /cloudcore/1.0/orders/` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-all-orders) |
| [List Products](actions/list-products.md) | `POST /cloudcore/1.0/products` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-all-products) |
| [List Shipping Countries](actions/list-shipping-countries.md) | `POST /cloudcore/1.0/shipping/countries` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-shipping-countries) |
| [List Shipping Levels](actions/list-shipping-levels.md) | `POST /cloudcore/1.0/shipping/levels` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-shipping-levels) |
| [List Shipping States](actions/list-shipping-states.md) | `POST /cloudcore/1.0/shipping/states` | [docs](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#list-shipping-states) |
