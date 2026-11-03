# Rithum for Brands: Native API Reference

A consolidated summary of Rithum for Brands's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://knowledge.channeladvisor.com/kc?id=kb_category_main&kb_knowledge_base=fdc1945887cf4910b535a7183cbb35bd
- **API base URL:** `https://api.channeladvisor.com/v1/`

## Authentication

### Refresh Token

Use a manually generated Refresh Token

### Credentials

- **Refresh Token:** `refreshToken` · optional
- **Application ID:** `applicationID` · optional
- **Shared Secret:** `sharedSecret` · optional

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=f2139601339696905ee4e7382e5c7bc3)

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.channeladvisor.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.channeladvisor.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `orders inventory`.

Refresh expired access tokens with a POST request to https://api.channeladvisor.com/oauth2/token.

[Official authentication documentation](https://api.channeladvisor.com/apidocs#tag/Guides/API-Authentication-Guide/Requesting-Authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–100). Use `$skip` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Product Export Status](actions/check-product-export-status.md) | `GET ProductExport` | [docs](https://api.channeladvisor.com/apidocs#tag/ProductExport/operation/ProductExport_CheckStatus) |
| [Check Product Upload Status](actions/check-product-upload-status.md) | `GET ProductUpload` | [docs](https://api.channeladvisor.com/apidocs#tag/ProductUpload/operation/ProductUpload_CheckStatus) |
| [Create a Product](actions/create-a-product.md) | `POST Products` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=1bdc17c52fd15994cffb5ff62799b6e9) |
| [Create Item Fulfilment](actions/create-item-fulfilment.md) | `POST Fulfillments` | [docs](https://api.channeladvisor.com/apidocs#tag/Fulfillments/operation/Fulfillments.Fulfillment.CreateFulfillment) |
| [Create Order](actions/create-order.md) | `POST Orders/Create` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=ae5173583304e290ae51a5373e5c7b5f&spa=1#concept-1655__section-49793) |
| [Delete Product Quantity](actions/delete-product-quantity.md) | `DELETE Products(:id)/DCQuantities(:distributionCenterID)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=21dcd3491bd5d1d42d9eea40604bcbdf#concept-8661__section-DistributionCenterQuantities) |
| [Get Order](actions/get-order.md) | `GET Orders(:orderID)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=f00d5fc52fd15994cffb5ff62799b68f) |
| [Get Order Fulfillments](actions/get-order-fulfillments.md) | `GET Orders(:orderID)/Fulfillments` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=981a17a187001e10712797d83cbb3550) |
| [Get Product](actions/get-product.md) | `GET Products(:id)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=21dcd3491bd5d1d42d9eea40604bcbdf) |
| [List Fulfillments](actions/list-fulfillments.md) | `GET Fulfillments(:fullfillmentID)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=13fcdf491bd5d1d42d9eea40604bcb65) |
| [List Order Items](actions/list-order-items.md) | `GET Orders(:orderID)/Items` |  |
| [List Orders](actions/list-orders.md) | `GET Orders` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=f00d5fc52fd15994cffb5ff62799b68f) |
| [List Product Quantities](actions/list-product-quantities.md) | `GET Products(:prodID)/DCQuantities` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=18ecd7491bd5d1d42d9eea40604bcb55) |
| [List Products](actions/list-products.md) | `GET Products` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=21dcd3491bd5d1d42d9eea40604bcbdf) |
| [List Profiles](actions/list-profiles.md) | `GET Profiles` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=b51d5f891bd5d1d42d9eea40604bcb57) |
| [List Sites](actions/list-sites.md) | `GET Sites` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=8600d6c8877e8e50712797d83cbb350f) |
| [Mark Order Exported](actions/post-order-exported.md) | `POST Orders(:orderID)/Export` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=f00d5fc52fd15994cffb5ff62799b68f) |
| [Mark Order Not Exported](actions/post-order-not-exported.md) | `DELETE Orders(:orderID)/Export` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=f00d5fc52fd15994cffb5ff62799b68f) |
| [Ship Order](actions/ship-order.md) | `POST Orders(:orderId)/Ship` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=b20d13092fd15994cffb5ff62799b602) |
| [Start Product Export](actions/start-product-export.md) | `POST ProductExport` | [docs](https://api.channeladvisor.com/apidocs#tag/ProductExport/operation/ProductExport.ExportFile) |
| [Update Item Fullfilment](actions/update-item-fullfilment.md) | `PATCH Fulfillments(:fullfilmentID)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=13fcdf491bd5d1d42d9eea40604bcb65) |
| [Update Order](actions/update-order.md) | `PATCH Orders(:id)` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=981a17a187001e10712797d83cbb3550) |
| [Update Product Quantity](actions/update-product-quantity.md) | `POST Products(:productID)/UpdateQuantity` | [docs](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_kb_id=c0ec1b491bd5d1d42d9eea40604bcb8d) |
| [Upload Product File](actions/upload-product-file.md) | `POST ProductUpload` | [docs](https://api.channeladvisor.com/apidocs#tag/ProductUpload/operation/ProductUpload_UploadFile) |
