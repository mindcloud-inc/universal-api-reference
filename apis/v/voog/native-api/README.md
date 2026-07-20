# Voog: Native API Reference

A consolidated summary of Voog's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.voog.com/developers/api
- **API base URL:** `{siteUrl}/admin/api`

## Authentication

### API Token

Authenticate to a specific Voog site with the site URL and an API token generated from Account > My profile.

### Credentials

- **API Key:** `apiKey` · required
- **Site URL:** `siteUrl` · required · Enter the full site origin without a trailing slash. The app will call {{credentials.siteUrl}}/admin/api.

Send these headers with each API request:

```http
X-API-TOKEN: <apiKey>
```

[Official authentication documentation](https://www.voog.com/developers/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Asset Upload](actions/confirm-asset-upload.md) | `PUT /assets/:assetId/confirm` | [docs](https://www.voog.com/developers/api/resources/assets) |
| [Create Article](actions/create-article.md) | `POST /articles` | [docs](https://www.voog.com/developers/api/resources/articles) |
| [Create Asset](actions/create-asset.md) | `POST /assets` | [docs](https://www.voog.com/developers/api/resources/assets) |
| [Create Category](actions/create-category.md) | `POST /ecommerce/v1/categories` | [docs](https://www.voog.com/developers/api/ecommerce/categories) |
| [Create Page](actions/create-page.md) | `POST /pages` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [Create Product](actions/create-product.md) | `POST /ecommerce/v1/products` | [docs](https://www.voog.com/developers/api/ecommerce/products) |
| [Create Site User](actions/create-site-user.md) | `POST /site_users` | [docs](https://www.voog.com/developers/api/resources/site_users) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://www.voog.com/developers/api/resources/webhooks) |
| [Delete Article](actions/delete-article.md) | `DELETE /articles/:articleId` | [docs](https://www.voog.com/developers/api/resources/articles) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /assets/:assetId` | [docs](https://www.voog.com/developers/api/resources/assets) |
| [Delete Category](actions/delete-category.md) | `DELETE /ecommerce/v1/categories/:categoryId` | [docs](https://www.voog.com/developers/api/ecommerce/categories) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/:pageId` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [Delete Product](actions/delete-product.md) | `DELETE /ecommerce/v1/products/:productId` | [docs](https://www.voog.com/developers/api/ecommerce/products) |
| [Delete Site User](actions/delete-site-user.md) | `DELETE /site_users/:siteUserId` | [docs](https://www.voog.com/developers/api/resources/site_users) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://www.voog.com/developers/api/resources/webhooks) |
| [Duplicate Page](actions/duplicate-page.md) | `POST /pages/:pageId/duplicate` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [Get Article](actions/get-article.md) | `GET /articles/:articleId` | [docs](https://www.voog.com/developers/api/resources/articles) |
| [Get Asset](actions/get-asset.md) | `GET /assets/:assetId` | [docs](https://www.voog.com/developers/api/resources/assets) |
| [Get Category](actions/get-category.md) | `GET /ecommerce/v1/categories/:categoryId` | [docs](https://www.voog.com/developers/api/ecommerce/categories) |
| [Get Order](actions/get-order.md) | `GET /ecommerce/v1/orders/:orderId` | [docs](https://www.voog.com/developers/api/ecommerce/orders) |
| [Get Order Shipping Method](actions/get-order-shipping-method.md) | `GET /ecommerce/v1/orders/:orderId/shipping_method` | [docs](https://www.voog.com/developers/api/ecommerce/orders) |
| [Get Page](actions/get-page.md) | `GET /pages/:pageId` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [Get Product](actions/get-product.md) | `GET /ecommerce/v1/products/:productId` | [docs](https://www.voog.com/developers/api/ecommerce/products) |
| [Get Site User](actions/get-site-user.md) | `GET /site_users/:siteUserId` | [docs](https://www.voog.com/developers/api/resources/site_users) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://www.voog.com/developers/api/resources/webhooks) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://www.voog.com/developers/api/resources/articles) |
| [List Assets](actions/list-assets.md) | `GET /assets` | [docs](https://www.voog.com/developers/api/resources/assets) |
| [List Categories](actions/list-categories.md) | `GET /ecommerce/v1/categories` | [docs](https://www.voog.com/developers/api/ecommerce/categories) |
| [List My Sites](actions/list-my-sites.md) | `GET /me/sites` | [docs](https://www.voog.com/developers/api/resources/me/sites) |
| [List Orders](actions/list-orders.md) | `GET /ecommerce/v1/orders` | [docs](https://www.voog.com/developers/api/ecommerce/orders) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [List Products](actions/list-products.md) | `GET /ecommerce/v1/products` | [docs](https://www.voog.com/developers/api/ecommerce/products) |
| [List Site Users](actions/list-site-users.md) | `GET /site_users` | [docs](https://www.voog.com/developers/api/resources/site_users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.voog.com/developers/api/resources/webhooks) |
| [Update Article](actions/update-article.md) | `PUT /articles/:articleId` | [docs](https://www.voog.com/developers/api/resources/articles) |
| [Update Category](actions/update-category.md) | `PUT /ecommerce/v1/categories/:categoryId` | [docs](https://www.voog.com/developers/api/ecommerce/categories) |
| [Update Order](actions/update-order.md) | `PUT /ecommerce/v1/orders/:orderId` | [docs](https://www.voog.com/developers/api/ecommerce/orders) |
| [Update Page](actions/update-page.md) | `PUT /pages/:pageId` | [docs](https://www.voog.com/developers/api/resources/pages) |
| [Update Product](actions/update-product.md) | `PUT /ecommerce/v1/products/:productId` | [docs](https://www.voog.com/developers/api/ecommerce/products) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhookId` | [docs](https://www.voog.com/developers/api/resources/webhooks) |
