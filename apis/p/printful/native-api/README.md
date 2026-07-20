# Printful: Native API Reference

A consolidated summary of Printful's API configuration and 55 documented operations, with links to official documentation.

- **Official docs:** https://developers.printful.com/docs/
- **API base URL:** `https://api.printful.com`

## Authentication

### Private Token

Use a Printful private token. Printful authenticates API requests with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.printful.com/docs/#section/Authorization/Private-tokens-and-public-apps)

## API conventions

Response data is read from `result`.

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File](actions/add-file.md) | `POST /files` | [docs](https://developers.printful.com/docs/#tag/File-Library-API/operation/addFile) |
| [Calculate Shipping Rates](actions/calculate-shipping-rates.md) | `POST /shipping/rates` | [docs](https://developers.printful.com/docs/#tag/Shipping-Rate-API/operation/calculateShippingRates) |
| [Calculate Tax Rates](actions/calculate-tax-rates.md) | `POST /tax/rates` | [docs](https://developers.printful.com/docs/#tag/Tax-Rate-API/operation/calculateTaxRates) |
| [Cancel Order](actions/cancel-order.md) | `DELETE /orders/{id}` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/cancelOrderById) |
| [Change Packing Slip](actions/change-packing-slip.md) | `POST /store/packing-slip` | [docs](https://developers.printful.com/docs/#tag/Store-Information-API/operation/changePackingSlip) |
| [Confirm Order](actions/confirm-order.md) | `POST /orders/{id}/confirm` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/confirmOrderById) |
| [Create Approval Sheet](actions/create-approval-sheet.md) | `POST /approval-sheets` | [docs](https://developers.printful.com/docs/#tag/Approval-Sheets-API/operation/approveDesign) |
| [Create Mockup Task](actions/create-mockup-task.md) | `POST /mockup-generator/create-task/{id}` | [docs](https://developers.printful.com/docs/#tag/Mockup-Generator-API/operation/createGeneratorTask) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/createOrder) |
| [Create Store Product](actions/create-store-product.md) | `POST /store/products` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/createSyncProduct) |
| [Create Store Variant](actions/create-store-variant.md) | `POST /store/products/{id}/variants` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/createSyncVariant) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.printful.com/docs/#tag/Webhook-API/operation/createWebhook) |
| [Delete Product Template](actions/delete-product-template.md) | `DELETE /product-templates/{id}` | [docs](https://developers.printful.com/docs/#tag/Product-Templates-API/operation/deleteProductTemplate) |
| [Delete Store Product](actions/delete-store-product.md) | `DELETE /store/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/deleteSyncProduct) |
| [Delete Store Variant](actions/delete-store-variant.md) | `DELETE /store/variants/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/deleteSyncVariant) |
| [Delete Sync Product](actions/delete-sync-product.md) | `DELETE /sync/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/deleteStoreSyncProduct) |
| [Delete Sync Variant](actions/delete-sync-variant.md) | `DELETE /sync/variant/{id}` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/deleteStoreSyncVariant) |
| [Disable Webhook](actions/disable-webhook.md) | `DELETE /webhooks` | [docs](https://developers.printful.com/docs/#tag/Webhook-API/operation/disableWebhook) |
| [Estimate Order Costs](actions/estimate-order-costs.md) | `POST /orders/estimate-costs` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/estimateOrderCosts) |
| [Get Approval Sheets](actions/get-approval-sheets.md) | `GET /approval-sheets` | [docs](https://developers.printful.com/docs/#tag/Approval-Sheets-API/operation/getApprovalSheets) |
| [Get Catalog Product](actions/get-catalog-product.md) | `GET /products/{id}` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getProductById) |
| [Get Catalog Variant](actions/get-catalog-variant.md) | `GET /products/variant/{id}` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getVariantById) |
| [Get Category](actions/get-category.md) | `GET /categories/{id}` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getCategoryById) |
| [Get File](actions/get-file.md) | `GET /files/{id}` | [docs](https://developers.printful.com/docs/#tag/File-Library-API/operation/getFile) |
| [Get Mockup Printfiles](actions/get-mockup-printfiles.md) | `GET /mockup-generator/printfiles/{id}` | [docs](https://developers.printful.com/docs/#tag/Mockup-Generator-API/operation/getPrintfiles) |
| [Get Mockup Task](actions/get-mockup-task.md) | `GET /mockup-generator/task` | [docs](https://developers.printful.com/docs/#tag/Mockup-Generator-API/operation/getTask) |
| [Get Mockup Templates](actions/get-mockup-templates.md) | `GET /mockup-generator/templates/{id}` | [docs](https://developers.printful.com/docs/#tag/Mockup-Generator-API/operation/getTemplates) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/getOrderById) |
| [Get Product Size Guide](actions/get-product-size-guide.md) | `GET /products/{id}/sizes` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getProductSizeGuideById) |
| [Get Product Template](actions/get-product-template.md) | `GET /product-templates/{id}` | [docs](https://developers.printful.com/docs/#tag/Product-Templates-API/operation/getProductTemplateById) |
| [Get Statistics](actions/get-statistics.md) | `GET /reports/statistics` | [docs](https://developers.printful.com/docs/#tag/Reports-API/operation/getStatistics) |
| [Get Store](actions/get-store.md) | `GET /stores/{id}` | [docs](https://developers.printful.com/docs/#tag/Store-Information-API/operation/getStore) |
| [Get Store Product](actions/get-store-product.md) | `GET /store/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/getSyncProductById) |
| [Get Store Variant](actions/get-store-variant.md) | `GET /store/variants/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/getSyncVariantById) |
| [Get Sync Product](actions/get-sync-product.md) | `GET /sync/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/getStoreSyncProductById) |
| [Get Sync Variant](actions/get-sync-variant.md) | `GET /sync/variant/{id}` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/getStoreSyncVariantById) |
| [Get Warehouse Product](actions/get-warehouse-product.md) | `GET /warehouse/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Warehouse-Products-API/operation/getWarehouseProduct) |
| [List Catalog Products](actions/list-catalog-products.md) | `GET /products` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getProducts) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://developers.printful.com/docs/#tag/Catalog-API/operation/getCategories) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://developers.printful.com/docs/#tag/CountryState-Code-API/operation/getCountries) |
| [List OAuth Scopes](actions/list-o-auth-scopes.md) | `GET /oauth/scopes` | [docs](https://developers.printful.com/docs/#tag/OAuth-API/operation/getScopes) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/getOrders) |
| [List Product Templates](actions/list-product-templates.md) | `GET /product-templates` | [docs](https://developers.printful.com/docs/#tag/Product-Templates-API/operation/getProductTemplates) |
| [List Store Products](actions/list-store-products.md) | `GET /store/products` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/getSyncProducts) |
| [List Stores](actions/list-stores.md) | `GET /stores` | [docs](https://developers.printful.com/docs/#tag/Store-Information-API/operation/getStores) |
| [List Sync Products](actions/list-sync-products.md) | `GET /sync/products` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/getStoreSyncProducts) |
| [List Tax Countries](actions/list-tax-countries.md) | `GET /tax/countries` | [docs](https://developers.printful.com/docs/#tag/Tax-Rate-API/operation/getTaxCountries) |
| [List Warehouse Products](actions/list-warehouse-products.md) | `GET /warehouse/products` | [docs](https://developers.printful.com/docs/#tag/Warehouse-Products-API/operation/getWarehouseProducts) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.printful.com/docs/#tag/Webhook-API/operation/getWebhooks) |
| [Submit Approval Sheet Changes](actions/submit-approval-sheet-changes.md) | `POST /approval-sheets/changes` | [docs](https://developers.printful.com/docs/#tag/Approval-Sheets-API/operation/submitApprovalSheetChanges) |
| [Suggest Thread Colors](actions/suggest-thread-colors.md) | `POST /files/thread-colors` | [docs](https://developers.printful.com/docs/#tag/File-Library-API/operation/threadColors) |
| [Update Order](actions/update-order.md) | `PUT /orders/{id}` | [docs](https://developers.printful.com/docs/#tag/Orders-API/operation/updateOrderById) |
| [Update Store Product](actions/update-store-product.md) | `PUT /store/products/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/updateSyncProduct) |
| [Update Store Variant](actions/update-store-variant.md) | `PUT /store/variants/{id}` | [docs](https://developers.printful.com/docs/#tag/Products-API/operation/updateSyncVariant) |
| [Update Sync Variant](actions/update-sync-variant.md) | `PUT /sync/variant/{id}` | [docs](https://developers.printful.com/docs/#tag/Ecommerce-Platform-Sync-API/operation/updateStoreSyncVariant) |
