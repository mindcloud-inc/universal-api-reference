# Botbaba: Native API Reference

A consolidated summary of Botbaba's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.botbaba.io/swagger/ui/index
- **OpenAPI specification:** https://app.botbaba.io/swagger/docs/v1
- **API base URL:** `https://app.botbaba.io`

## Authentication

### Auth Token

Use the auth token generated from the My Profile page in Botbaba.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://kb.botbaba.io/docs/how-to-obtain-auth-token-or-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot User](actions/create-bot-user.md) | `POST /api/InsertBotUser` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Create Product](actions/create-product.md) | `POST /api/InsertProduct` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Create Product Category](actions/create-product-category.md) | `POST /api/InsertProductCategory` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Get Blocks](actions/get-blocks.md) | `GET /api/GetBlocks` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Get Bot User](actions/get-bot-user.md) | `GET /api/GetBotUserById` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Get Bot Widget Settings](actions/get-bot-widget-settings.md) | `GET /api/GetBotWidgetSettings` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Get Product](actions/get-product.md) | `GET /api/GetProductById` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Get Product Category](actions/get-product-category.md) | `GET /api/GetProductCategoryById` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List Bot Conversations](actions/list-bot-conversations.md) | `GET /api/GetBotConversations` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List Bot Tags](actions/list-bot-tags.md) | `GET /api/GetBotTags` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List Bots](actions/list-bots.md) | `GET /api/GetBots` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List Product Categories](actions/list-product-categories.md) | `GET /api/GetProductCategories` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List Products](actions/list-products.md) | `GET /api/GetProducts` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [List User Fields](actions/list-user-fields.md) | `GET /api/GetUserFields` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Set Product Active Status](actions/set-product-active-status.md) | `POST /api/EditProductActiveStatus` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Set Product Category Active Status](actions/set-product-category-active-status.md) | `POST /api/EditProductCategoryActiveStatus` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Update Product](actions/update-product.md) | `POST /api/EditProduct` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Update Product Category](actions/update-product-category.md) | `POST /api/EditProductCategory` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Update Product Inventory](actions/update-product-inventory.md) | `POST /api/EditProductInventory` | [docs](https://app.botbaba.io/swagger/ui/index) |
| [Update Product Inventory Total](actions/update-product-inventory-total.md) | `POST /api/EditProductInventoryTotal` | [docs](https://app.botbaba.io/swagger/ui/index) |
