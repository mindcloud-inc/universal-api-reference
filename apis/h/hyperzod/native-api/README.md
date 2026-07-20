# Hyperzod: Native API Reference

A consolidated summary of Hyperzod's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550
- **OpenAPI specification:** https://archbee-doc-uploads.s3.amazonaws.com/A6k4A417O1V2DGm4H5kN0/bBGM0lJYbsaQKkZKCMccO-20250926-063409.json
- **API base URL:** `https://api.hyperzod.app`

## Authentication

### API Key

Connect to Hyperzod with an API key and tenant ID.

### Credentials

- **API Key:** `apiKey` · required
- **Tenant ID:** `tenantId` · required · Tenant ID from Settings > API Keys & Webhooks.

Send these headers with each API request:

```http
X-TENANT: <tenantId>
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-TL98Hc7vz_lSnqPXcK8rY)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `data.last_page`. The current page number is read from `data.current_page`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Product Inventory](actions/bulk-update-product-inventory.md) | `POST /merchant/v1/catalog/product/stock/updateCountBulk` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-pTZC-McWO7Rr2uAhvZZLY) |
| [Create Address](actions/create-address.md) | `POST /admin/v1/address/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-osZ5KYwLg5Bs0GbS5wOjT) |
| [Create Customer](actions/create-customer.md) | `POST /admin/v1/auth/user/add` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-n8xkoB1wPumD9sNiAEpcw) |
| [Create Merchant](actions/create-merchant.md) | `POST /admin/v1/merchant/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-m0a9hfOaR8z9rC5nrVTc6) |
| [Create Merchant Category](actions/create-merchant-category.md) | `POST /admin/v1/merchant/merchant-categories/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-0Ja4wdYw4I7nhjrla7UGO) |
| [Create Order](actions/create-order.md) | `POST /admin/v1/order/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-jvGMncaJgUffXZAiP-JrL) |
| [Create Order Note](actions/create-order-note.md) | `POST /admin/v1/order/addNote` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-YrCGQpnkzPj9BRqyD7tqz) |
| [Create Product](actions/create-product.md) | `POST /merchant/v1/catalog/product/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-oRVkZPysXV51nZpI0O1YK) |
| [Create Product Category](actions/create-product-category.md) | `POST /merchant/v1/catalog/product-category/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-KCE6wskRSRmZUBGrwK6b4) |
| [Create Product Label](actions/create-product-label.md) | `POST /merchant/v1/catalog/product-label/create` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-x7XuWpAwpBT60Y4iG1yiP) |
| [Delete Address](actions/delete-address.md) | `POST /admin/v1/address/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-4Zo8r_efKh--Yb5UqyJSG) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /admin/v1/auth/user/:id` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-y6JfiU3Pwjiae-dQuT73V) |
| [Delete Merchant](actions/delete-merchant.md) | `POST /admin/v1/merchant/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-KPhZyN7aLBWzzEqRq6_r0) |
| [Delete Merchant Category](actions/delete-merchant-category.md) | `POST /admin/v1/merchant-categories/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-1Gf9cap7ofRS0uHRQQbMk) |
| [Delete Product](actions/delete-product.md) | `POST /merchant/v1/catalog/product/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-lfdLXW4VvPaJYu104ddJH) |
| [Delete Product Category](actions/delete-product-category.md) | `POST /merchant/v1/catalog/product-category/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-SVz3RrjDBtkusDuJ4QkYP) |
| [Delete Product Label](actions/delete-product-label.md) | `POST /merchant/v1/catalog/product-label/delete` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-F5-j1wjKz58x3AsDiYo2U) |
| [Fetch Address](actions/fetch-address.md) | `GET /admin/v1/address/fetch` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-jz1N_H9B8YfTljOQQk3fU) |
| [List Customers](actions/list-customers.md) | `GET /admin/v1/auth/user/all` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-jD-opR5GlOGxBOdLX_6wq) |
| [List Merchant Categories](actions/list-merchant-categories.md) | `GET /admin/v1/merchant/merchant-categories/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-9Sx1ZjzhNJF8Yi39Dvalf) |
| [List Merchants](actions/list-merchants.md) | `GET /admin/v1/merchant/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-4pbBOT8J6pFZ1Sl6VcuS5) |
| [List Order Commissions](actions/list-order-commissions.md) | `GET /admin/v1/order/commission` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-9ka5javifQ0-gmmWuhhh-) |
| [List Order Status](actions/list-order-status.md) | `GET /admin/v1/order/status/order` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-vD3JwcKU3vewmnJqhg4pt) |
| [List Orders](actions/list-orders.md) | `POST /admin/v1/order/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-KDJ690JUWLldCtw-_Tvic) |
| [List Product Categories](actions/list-product-categories.md) | `GET /merchant/v1/catalog/product-category/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-pgmdT8W6mKye0Px5WC5NV) |
| [List Product Labels](actions/list-product-labels.md) | `GET /merchant/v1/catalog/product-label/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-vogztZSTAP4SN1hzhDPfZ) |
| [List Products](actions/list-products.md) | `GET /merchant/v1/catalog/product/list` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-GNe3ocH78iV2b9SRTvjQ_) |
| [List Scheduled Orders](actions/list-scheduled-orders.md) | `POST /admin/v1/order/scheduled` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-OrHsa256mQFS3lktJgihe) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /admin/v1/order` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-sWc9Fu9lKhKcpfgKZPXUx) |
| [Retrieve Order Scheduling Slots](actions/retrieve-order-scheduling-slots.md) | `GET /admin/v1/order/scheduling-slots` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-QTyB-HCSAlDNi24wprTG7) |
| [Retrieve Order Stats](actions/retrieve-order-stats.md) | `GET /admin/v1/order/stats` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-C0-Qx9TbWU7QiuU1PDxCN) |
| [Retrieve Product Category](actions/retrieve-product-category.md) | `GET /merchant/v1/catalog/product-category/view` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-JQ5hMcuUbjjxFMefX858u) |
| [Retrieve Product Label](actions/retrieve-product-label.md) | `GET /merchant/v1/catalog/product-label/view` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-MgJxhn35hDnURsHquxlg8) |
| [Update Address](actions/update-address.md) | `POST /admin/v1/address/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-KG0rKChyrCJA7G9fu3b_S) |
| [Update Merchant](actions/update-merchant.md) | `POST /admin/v1/merchant/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-cO5P1NNydE189mQtPIsSl) |
| [Update Merchant Category](actions/update-merchant-category.md) | `POST /admin/v1/merchant/merchant-categories/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-qabiAz0RiOTUS_iAettkK) |
| [Update Order Status](actions/update-order-status.md) | `POST /admin/v1/order/update-order-status` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-oRjr4Ra9jokUbOODNApn9) |
| [Update Product](actions/update-product.md) | `POST /merchant/v1/catalog/product/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-9L_XY-i6ynVYz25hmynxQ) |
| [Update Product Category](actions/update-product-category.md) | `POST /merchant/v1/catalog/product-category/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-LD2cj4TsTkTJqF_w2c7CY) |
| [Update Product Label](actions/update-product-label.md) | `POST /merchant/v1/catalog/product-label/update` | [docs](https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550/PREVIEW-oTgu4mt1AKd1aNLjvxXb3) |
