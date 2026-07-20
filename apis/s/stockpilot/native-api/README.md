# Stockpilot: Native API Reference

A consolidated summary of Stockpilot's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://api.stockpilot.dev/redoc
- **OpenAPI specification:** https://api.stockpilot.dev/openapi.json
- **API base URL:** `https://api.stockpilot.dev`

## Authentication

### Client ID and Client Secret

Authenticate with your Stockpilot API client ID and client secret.

### Credentials

- **Client ID:** `clientId` · required · Your Stockpilot API client ID.
- **Client Secret:** `clientSecret` · required · Your Stockpilot API client secret.

Send these headers with each API request:

```http
X-CLIENT-ID: <clientId>
X-CLIENT-SECRET: <clientSecret>
```

[Official authentication documentation](https://api.stockpilot.dev/redoc)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | `PUT /orders/cancel-order` | [docs](https://api.stockpilot.dev/redoc#operation/cancel_order_orders_cancel_order_put) |
| [Create Brand](actions/create-brand.md) | `POST /brands/create` | [docs](https://api.stockpilot.dev/redoc#operation/create_brand_brands_create_post) |
| [Create Category](actions/create-category.md) | `POST /categories/create` | [docs](https://api.stockpilot.dev/redoc#operation/create_category_categories_create_post) |
| [Create Inventory Item](actions/create-inventory-item.md) | `POST /inventory/create` | [docs](https://api.stockpilot.dev/redoc#operation/create_inventory_inventory_create_post) |
| [Create Order](actions/create-order.md) | `POST /orders/create` | [docs](https://api.stockpilot.dev/redoc#operation/create_order_orders_create_post) |
| [Create Product](actions/create-product.md) | `POST /products/create` | [docs](https://api.stockpilot.dev/redoc#operation/create_product_products_create_post) |
| [Delete Entire Order](actions/delete-entire-order.md) | `DELETE /orders/:order_id` | [docs](https://api.stockpilot.dev/redoc#operation/delete_order_orders__order_id__delete) |
| [Fulfil Order](actions/fulfil-order.md) | `POST /orders/fulfil` | [docs](https://api.stockpilot.dev/redoc#operation/fulfil_order_orders_fulfil_post) |
| [Get Fulfillment Details](actions/get-fulfillment-details.md) | `GET /orders/fulfillment` | [docs](https://api.stockpilot.dev/redoc#operation/get_fulfillment_details_orders_fulfillment_get) |
| [Get Inventory Item](actions/get-inventory-item.md) | `GET /inventory/get` | [docs](https://api.stockpilot.dev/redoc#operation/get_inventory_item_inventory_get_get) |
| [Get Invoice for Order](actions/get-invoice-for-order.md) | `GET /invoices/get/:order_pk` | [docs](https://api.stockpilot.dev/redoc#operation/get_invoice_invoices_get__order_pk__get) |
| [Get Item Sales Analytics](actions/get-item-sales-analytics.md) | `GET /analytics/items/sales` | [docs](https://api.stockpilot.dev/redoc#operation/get_item_sales_analytics_analytics_items_sales_get) |
| [Get Label Suggestion](actions/get-label-suggestion.md) | `GET /shipping/label-suggestion` | [docs](https://api.stockpilot.dev/redoc#operation/get_shipping_label_suggestion_shipping_label_suggestion_get) |
| [Get Product by ID](actions/get-product-by-id.md) | `GET /products/get` | [docs](https://api.stockpilot.dev/redoc#operation/get_product_products_get_get) |
| [Get Sales Summary](actions/get-sales-summary.md) | `GET /analytics/sales-summary` | [docs](https://api.stockpilot.dev/redoc#operation/get_sales_summary_analytics_sales_summary_get) |
| [Get Single Order](actions/get-single-order.md) | `GET /orders/get-single` | [docs](https://api.stockpilot.dev/redoc#operation/get_single_order_orders_get_single_get) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://api.stockpilot.dev/redoc#operation/get_brands_brands_get) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://api.stockpilot.dev/redoc#operation/get_categories_categories_get) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api.stockpilot.dev/redoc#operation/list_customers_customers_get) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /inventory` | [docs](https://api.stockpilot.dev/redoc#operation/get_inventory_list_inventory_get) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://api.stockpilot.dev/redoc#operation/get_orders_list_orders_get) |
| [List Orders with Cancellation Requests](actions/list-orders-with-cancellation-requests.md) | `GET /orders/cancellation-requests` | [docs](https://api.stockpilot.dev/redoc#operation/get_cancellation_requests_orders_cancellation_requests_get) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api.stockpilot.dev/redoc#operation/get_product_list_products_get) |
| [List Sales Channels](actions/list-sales-channels.md) | `GET /sales-channels` | [docs](https://api.stockpilot.dev/redoc#operation/get_channels_sales_channels_get) |
| [List Shipping Integrations](actions/list-shipping-integrations.md) | `GET /shipping/integrations` | [docs](https://api.stockpilot.dev/redoc#operation/get_shipping_integrations_shipping_integrations_get) |
| [List Suppliers](actions/list-suppliers.md) | `GET /purchase-orders/suppliers/list` | [docs](https://api.stockpilot.dev/redoc#operation/get_suppliers_list_purchase_orders_suppliers_list_get) |
| [List Warehouse Items](actions/list-warehouse-items.md) | `GET /warehouses/:unique_id/items` | [docs](https://api.stockpilot.dev/redoc#operation/get_warehouses_items_warehouses__unique_id__items_get) |
| [List Warehouses](actions/list-warehouses.md) | `GET /warehouses/get` | [docs](https://api.stockpilot.dev/redoc#operation/get_warehouses_list_warehouses_get_get) |
| [Request Shipping Label](actions/request-shipping-label.md) | `POST /shipping/request-label` | [docs](https://api.stockpilot.dev/redoc#operation/request_label_shipping_request_label_post) |
| [Retrieve Shipping Label](actions/retrieve-shipping-label.md) | `POST /shipping/retrieve-label` | [docs](https://api.stockpilot.dev/redoc#operation/retrieve_label_shipping_retrieve_label_post) |
| [Send Invoice](actions/send-invoice.md) | `POST /invoices/send` | [docs](https://api.stockpilot.dev/redoc#operation/send_invoice_invoices_send_post) |
| [Update Inventory Item](actions/update-inventory-item.md) | `POST /inventory/update` | [docs](https://api.stockpilot.dev/redoc#operation/update_inventory_inventory_update_post) |
| [Update Order Status](actions/update-order-status.md) | `PATCH /orders/:order_id/update-status` | [docs](https://api.stockpilot.dev/redoc#operation/update_order_status_orders__order_id__update_status_patch) |
| [Update Ordered Item Details](actions/update-ordered-item-details.md) | `PATCH /orders/ordered-items/:item_id/update` | [docs](https://api.stockpilot.dev/redoc#operation/update_ordered_item_orders_ordered_items__item_id__update_patch) |
| [Verify API Credentials](actions/verify-api-credentials.md) | `GET /auth/who-is` | [docs](https://api.stockpilot.dev/redoc#operation/who_is_auth_who_is_get) |
