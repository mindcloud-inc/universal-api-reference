# TikTok Shop: Native API Reference

A consolidated summary of TikTok Shop's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://partner.tiktokshop.com/docv2/page/666012dd609d4402cc3be995?external_id=666012dd609d4402cc3be995
- **API base URL:** `https://open-api.tiktokglobalshop.com/`

## Authentication

### Use your own TikTok App

### Credentials

- **Service Id:** `serviceId` · optional
- **App Key:** `appKey` · optional
- **App Secret:** `appSecret` · optional

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://services.us.tiktokshop.com/open/authorize to approve access.
2. Exchange the returned authorization code with a GET request to https://auth.tiktok-shops.com/api/v2/token/get.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a GET request to https://auth.tiktok-shops.com/api/v2/token/refresh.

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_key` | query | `string` | no |

The next-page cursor is read from `data.nextPageToken`. The total page count is read from `data.totalCount`.

## Pagination

Use `page_size` in the query string to set the page size (default 20; accepted range 1–100). Use `page_token` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | `POST return_refund/202309/cancellations` | [docs](https://partner.tiktokshop.com/docv2/page/cancel-order-202309) |
| [Create Packages](actions/create-packages.md) | `POST fulfillment/202309/packages` | [docs](https://partner.tiktokshop.com/docv2/page/650aa132bace3e02b75d40d8?external_id=650aa132bace3e02b75d40d8#Back%20To%20Top) |
| [Create Product](actions/create-product.md) | `POST /product/202309/products` | [docs](https://partner.us.tiktokshop.com/dev/api-testing-tool?apiId=7262710099251201798&pkgId=431492&versionId=202309) |
| [Get Authorized Shops](actions/get-authorized-shops.md) | `GET https://open-api.tiktokglobalshop.com/authorization/202309/shops` | [docs](https://partner.tiktokshop.com/docv2/page/6507ead7b99d5302be949ba9?external_id=6507ead7b99d5302be949ba9) |
| [Get Order Detail](actions/get-order-detail.md) | `GET order/202309/orders` | [docs](https://partner.tiktokshop.com/docv2/page/6507ead7b99d5302be949ba9?external_id=6507ead7b99d5302be949ba9) |
| [Get Order List](actions/get-order-list.md) | `POST order/202309/orders/search` | [docs](https://partner.tiktokshop.com/docv2/page/650aa8094a0bb702c06df242?external_id=650aa8094a0bb702c06df242) |
| [Get Package Detail](actions/get-package-detail.md) | `GET fulfillment/202309/packages/:packageID` | [docs](https://partner.tiktokshop.com/docv2/page/get-package-detail-202309#Back%20To%20Top) |
| [Get Package Shipping Document](actions/get-package-shipping-document.md) | `GET fulfillment/202309/packages/:packageId/shipping_documents` | [docs](https://partner.tiktokshop.com/docv2/page/get-package-shipping-document-202309) |
| [Get Package Shipping Document (v2)](actions/get-package-shipping-document-v2.md) | `GET /fulfillment/202309/packages/:package_id/shipping_documents` | [docs](https://partner.tiktokshop.com/docv2/page/6507ead7b99d5302be949ba9?external_id=6507ead7b99d5302be949ba9) |
| [Get Product](actions/get-product.md) | `GET product/202309/products/:product_id` | [docs](https://partner.tiktokshop.com/docv2/page/get-product-202309) |
| [Get Product Inventory](actions/get-product-inventory.md) | `POST product/202309/inventory/search` | [docs](https://partner.tiktokshop.com/doc/page/649a5faa600c3a0288889b35?external_id=649a5faa600c3a0288889b35#Back%20To%20Top) |
| [Get Shipping Providers](actions/get-shipping-providers.md) | `GET logistics/202309/delivery_options/:delivery_option_id/shipping_providers` | [docs](https://partner.tiktokshop.com/docv2/page/get-shipping-providers-202309) |
| [Get Statements](actions/get-statements.md) | `GET finance/202309/statements` | [docs](https://partner.tiktokshop.com/docv2/page/get-statements-202309) |
| [Get Transactions by Statement](actions/get-transactions-by-statement.md) | `GET finance/:version/statements/:statement_id/statement_transactions` | [docs](https://partner.tiktokshop.com/docv2/page/get-statements-202309) |
| [Get Warehouse Delivery Options](actions/get-warehouse-delivery-options.md) | `GET logistics/202309/warehouses/:warehouse_id/delivery_options` | [docs](https://partner.tiktokshop.com/docv2/page/get-warehouse-delivery-options-202309) |
| [Get Warehouse List](actions/get-warehouse-list.md) | `GET logistics/202309/warehouses` | [docs](https://partner.tiktokshop.com/docv2/page/get-warehouse-list-202309) |
| [List Eligible Shipping Service](actions/list-eligible-shipping-service.md) | `POST /fulfillment/202309/orders/:orderId/shipping_services/query` | [docs](https://partner.tiktokshop.com/docv2/page/650aa6b2bace3e02b75dda4e?external_id=650aa6b2bace3e02b75dda4e) |
| [Mark Package As Shipped](actions/mark-package-as-shipped.md) | `POST fulfillment/202309/orders/:order_id/packages` | [docs](https://partner.tiktokshop.com/docv2/page/mark-package-as-shipped) |
| [Search Products](actions/search-products.md) | `POST product/202502/products/search` | [docs](https://partner.tiktokshop.com/docv2/page/search-products-202502) |
| [Ship Package](actions/ship-package.md) | `POST fulfillment/202309/packages/:package_id/ship` | [docs](https://partner.tiktokshop.com/docv2/page/ship-package-202309) |
| [Split Orders](actions/split-orders.md) | `POST fulfillment/202309/orders/:order_id/split` | [docs](https://partner.tiktokshop.com/docv2/page/split-orders-202309) |
| [Update Inventory](actions/update-inventory.md) | `POST product/202309/products/:product_id/inventory/update` | [docs](https://partner.tiktokshop.com/doc/page/63fd742b715d622a338c4bbf?external_id=63fd742b715d622a338c4bbf) |
