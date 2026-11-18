# Temu: Native API Reference

A consolidated summary of Temu's API configuration and 6 documented operations.

- **API base URL:** `https://openapi-b-us.temu.com/openapi`

## Authentication

### Manual Authorization

### Credentials

- **Access Token:** `accessToken` · required
- **App Key:** `appKey` · required
- **App Secret:** `appSecret` · required

[Official authentication documentation](https://partner-us.temu.com/documentation?menu_code=38e79b35d2cb463d85619c1c786dd303&sub_menu_code=1e91f4383a8340c2b98780acc34fa6ec)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the request body to set the page size (default 10; accepted range 1–100). Use `pageNumber` in the request body to choose the page; numbering starts at 1.

## Sorting

Send sorting in the request body. Only one sort field is accepted.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Combined Shipping Groups](actions/get-combined-shipping-groups.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=67de1544d4ca4a8dbd78f57911a5159b) |
| [Get Order](actions/get-order.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=9bf33a25319e4d7bbaf5ece4b823b9c3) |
| [Get Order Address](actions/get-order-address.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=ccc2f59661584f5e8e205d85ddb9a6c9) |
| [Get Order Customization](actions/get-order-customization.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=e8f86a2f5241441e9b095bf309d04dce) |
| [List Local SKUs](actions/list-local-sk-us.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=0037738f728b4e81886d17511f2d4f0f) |
| [List Orders](actions/list-orders.md) | `POST /router` | [docs](https://partner-us.temu.com/documentation?menu_code=fb16b05f7a904765aac4af3a24b87d4a&sub_menu_code=554fd46b45ee49269cbdd6d4008a5dc1) |
