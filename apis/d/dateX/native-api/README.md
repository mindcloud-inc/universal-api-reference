# DateX (Legacy): Native API Reference

A consolidated summary of DateX (Legacy)'s API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://sku-mindcloud-api.wavelength.host/documentation/
- **OpenAPI specification:** https://sku-mindcloud-api.wavelength.host/documentation/swagger
- **API base URL:** `https://{environment}.wavelength.host/api/`

## Authentication

### Azure Client Credentials

Uses Azure OAuth2 client-credentials to acquire a bearer token for the DateX/SKU API, then sends Authorization: Bearer {{credentials.custom.accessToken}} on API requests.

### Credentials

- **Environment Host Prefix:** `environment` · required · Host prefix used in https://{{credentials.environment}}.wavelength.host/api/. For the documented sandbox API, use sku-mindcloud-api.
- **Scope:** `scope` · required
- **Client Secret:** `clientSecret` · required
- **Client Id:** `clientId` · required
- **Token Url:** `tokenUrl` · required

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

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | `POST sales_orders/create` | [docs](https://test-sku-mindcloud-api.wavelength.host/documentation/) |
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
| [Save Shipping Label](actions/save-shipping-label.md) | `POST packsize/save_shipping_label` |  |
| [Update Materials](actions/update-materials.md) | `POST materials/update` |  |
| [Update sale order shipment containers](actions/update-sale-order-shipment-containers.md) | `POST shipments/shipping_details/update` |  |
| [Update Sales Order](actions/update-sales-order.md) | `POST sales_orders/update` |  |
| [Update Shipment](actions/update-shipment.md) | `POST shipment/update` |  |
