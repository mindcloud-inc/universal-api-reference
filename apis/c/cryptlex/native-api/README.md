# Cryptlex: Native API Reference

A consolidated summary of Cryptlex's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.cryptlex.com/v3/docs
- **OpenAPI specification:** https://api.cryptlex.com/api-docs/v3/swagger.json
- **API base URL:** `https://api.cryptlex.com`

## Authentication

### Personal Access Token

Use a Cryptlex personal access token to authenticate REST API requests with a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.cryptlex.com/web-integrations/personal-access-tokens)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create License](actions/create-license.md) | `POST /v3/licenses` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/post/v3/licenses) |
| [Create Product](actions/create-product.md) | `POST /v3/products` | [docs](https://api.cryptlex.com/v3/docs#tag/Products/operation/post/v3/products) |
| [Create Release](actions/create-release.md) | `POST /v3/releases` | [docs](https://api.cryptlex.com/v3/docs#tag/Releases/operation/post/v3/releases) |
| [Create Release Platform](actions/create-release-platform.md) | `POST /v3/release-platforms` | [docs](https://api.cryptlex.com/v3/docs#tag/ReleasePlatforms/operation/post/v3/release-platforms) |
| [Create User](actions/create-user.md) | `POST /v3/users` | [docs](https://api.cryptlex.com/v3/docs#tag/Users/operation/post/v3/users) |
| [Create Webhook](actions/create-webhook.md) | `POST /v3/webhooks` | [docs](https://api.cryptlex.com/v3/docs#tag/Webhooks/operation/post/v3/webhooks) |
| [Extend License](actions/extend-license.md) | `POST /v3/licenses/:id/extend` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/post/v3/licenses/%7Bid%7D/extend) |
| [Get Activation](actions/get-activation.md) | `GET /v3/activations/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Activations/operation/get/v3/activations/%7Bid%7D) |
| [Get License](actions/get-license.md) | `GET /v3/licenses/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/get/v3/licenses/%7Bid%7D) |
| [Get Product](actions/get-product.md) | `GET /v3/products/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Products/operation/get/v3/products/%7Bid%7D) |
| [Get Release](actions/get-release.md) | `GET /v3/releases/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Releases/operation/get/v3/releases/%7Bid%7D) |
| [Get User](actions/get-user.md) | `GET /v3/users/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Users/operation/get/v3/users/%7Bid%7D) |
| [Get Webhook](actions/get-webhook.md) | `GET /v3/webhooks/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Webhooks/operation/get/v3/webhooks/%7Bid%7D) |
| [List Activations](actions/list-activations.md) | `GET /v3/activations` | [docs](https://api.cryptlex.com/v3/docs#tag/Activations/operation/get/v3/activations) |
| [List Licenses](actions/list-licenses.md) | `GET /v3/licenses` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/get/v3/licenses) |
| [List Products](actions/list-products.md) | `GET /v3/products` | [docs](https://api.cryptlex.com/v3/docs#tag/Products/operation/get/v3/products) |
| [List Releases](actions/list-releases.md) | `GET /v3/releases` | [docs](https://api.cryptlex.com/v3/docs#tag/Releases/operation/get/v3/releases) |
| [List Users](actions/list-users.md) | `GET /v3/users` | [docs](https://api.cryptlex.com/v3/docs#tag/Users/operation/get/v3/users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v3/webhooks` | [docs](https://api.cryptlex.com/v3/docs#tag/Webhooks/operation/get/v3/webhooks) |
| [Publish Release](actions/publish-release.md) | `POST /v3/releases/:id/publish` | [docs](https://api.cryptlex.com/v3/docs#tag/Releases/operation/post/v3/releases/%7Bid%7D/publish) |
| [Renew License](actions/renew-license.md) | `POST /v3/licenses/:id/renew` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/post/v3/licenses/%7Bid%7D/renew) |
| [Update License](actions/update-license.md) | `PATCH /v3/licenses/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Licenses/operation/patch/v3/licenses/%7Bid%7D) |
| [Update Product](actions/update-product.md) | `PATCH /v3/products/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Products/operation/patch/v3/products/%7Bid%7D) |
| [Update User](actions/update-user.md) | `PATCH /v3/users/:id` | [docs](https://api.cryptlex.com/v3/docs#tag/Users/operation/patch/v3/users/%7Bid%7D) |
