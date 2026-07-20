# DateX: Native API Reference

A consolidated summary of DateX's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://sku-mindcloud-api.wavelength.host/documentation/
- **OpenAPI specification:** https://sku-mindcloud-api.wavelength.host/documentation/swagger
- **API base URL:** `https://{environment}.wavelength.host/api/`

## Authentication

### Azure Client Credentials

Uses Azure OAuth2 client-credentials to acquire a bearer token for the DateX/SKU API, then sends Authorization: Bearer {{credentials.custom.accessToken}} on API requests.

### Credentials

- **Environment Host Prefix:** `environment` · required · Host prefix used in https://{{credentials.environment}}.wavelength.host/api/. For the documented sandbox API, use sku-mindcloud-api.
- **Scope:** `scope` · required · Azure API scope for DateX/SKU, ending in /.default.
- **Client Secret:** `clientSecret` · required · Azure application client secret.
- **Client ID:** `clientId` · required · Azure application client ID.
- **Token URL:** `tokenUrl` · required · Azure OAuth2 v2 token endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://sku-mindcloud-api.wavelength.host/documentation/custom.js)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON. The total page count is read from `paging.total_records`. The current page number is read from `paging.skip`.

## Pagination

Use `paging.top` in the request body to set the page size (default 50; accepted range 1–500). Use `paging.skip` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body. Supported operators: `between`, `contain`, `eq`, `gt`, `gte`, `lt`, `lte`, `ncontain`, `ne`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | `POST https://login.microsoftonline.com/6498fd5a-7169-49a0-a87e-2107759e83e2/oauth2/v2.0/token` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/custom.js) |
| [Create Sales Order Lines](actions/create-sales-order-lines.md) | `POST sales_order_lines/create` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_order_lines_create) |
| [Create Sales Orders](actions/create-sales-orders.md) | `POST sales_orders/create` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_create) |
| [Delete Shipment Transmissions](actions/delete-shipment-transmissions.md) | `POST sales_orders/shipments/transmissions/delete` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_shipments_transmissions_delete) |
| [Echo Test](actions/echo-test.md) | `POST echo_test` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_echo_test) |
| [List Available Inventory](actions/list-available-inventory.md) | `POST inventory_availability/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_inventory_availability_get) |
| [List Carriers](actions/list-carriers.md) | `POST carriers/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_carriers_get) |
| [List Inventory](actions/list-inventory.md) | `POST inventory/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_inventory_get) |
| [List Materials](actions/list-materials.md) | `POST materials/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_materials_get) |
| [List Owners](actions/list-owners.md) | `POST owners/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_owners_get) |
| [List Sales Orders](actions/list-sales-orders.md) | `POST sales_orders/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_get) |
| [List Sales Shipments](actions/list-sales-shipments.md) | `POST sales_orders/shipments/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_shipments_get) |
| [List Shipping Details](actions/list-shipping-details.md) | `POST shipments/shipping_details/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipments_shipping_details_get) |
| [List Warehouses](actions/list-warehouses.md) | `POST warehouses/get` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_warehouses_get) |
| [Update Sales Order Lines](actions/update-sales-order-lines.md) | `POST sales_order_lines/update` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_order_lines_update) |
| [Update Sales Orders](actions/update-sales-orders.md) | `POST sales_orders/update` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_update) |
| [Update Shipment Markup Cost](actions/update-shipment-markup-cost.md) | `POST shipment/update` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipment_update) |
| [Update Shipping Details](actions/update-shipping-details.md) | `POST shipments/shipping_details/update` | [docs](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipments_shipping_details_update) |
