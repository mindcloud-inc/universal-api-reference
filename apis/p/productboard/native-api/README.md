# Productboard: Native API Reference

A consolidated summary of Productboard's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://developer.productboard.com/reference
- **API base URL:** `https://api.productboard.com`

## Authentication

### API Key

Use a Productboard public API access token to authenticate requests to the Productboard REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.productboard.com/v2.0.0/reference/api-token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `X-Version` | `1` |

Responses from this API use JSON.

## Pagination

Follow the complete next-page URL returned by the API.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Component](actions/get-component.md) | `GET /components/:id` | [docs](https://developer.productboard.com/reference/getcomponent) |
| [Get Feature](actions/get-feature.md) | `GET /features/:id` | [docs](https://developer.productboard.com/reference/getfeature) |
| [Get Objective](actions/get-objective.md) | `GET /objectives/:id` | [docs](https://developer.productboard.com/reference/getobjective) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://developer.productboard.com/reference/getproduct) |
| [Get Release](actions/get-release.md) | `GET /releases/:id` | [docs](https://developer.productboard.com/reference/getrelease) |
| [List All Components](actions/list-all-components.md) | `GET /components` | [docs](https://developer.productboard.com/reference/getcomponents) |
| [List All Feature Statuses](actions/list-all-feature-statuses.md) | `GET /feature-statuses` | [docs](https://developer.productboard.com/reference/getfeaturestatuses) |
| [List All Features](actions/list-all-features.md) | `GET /features` | [docs](https://developer.productboard.com/reference/getfeatures) |
| [List All Notes](actions/list-all-notes.md) | `GET /notes` | [docs](https://developer.productboard.com/reference/getnotes) |
| [List All Objectives](actions/list-all-objectives.md) | `GET /objectives` | [docs](https://developer.productboard.com/reference/getobjectives) |
| [List All Products](actions/list-all-products.md) | `GET /products` | [docs](https://developer.productboard.com/reference/getproducts) |
| [List All Releases](actions/list-all-releases.md) | `GET /releases` | [docs](https://developer.productboard.com/reference/listreleases) |
| [List All Users](actions/list-all-users.md) | `GET /users` | [docs](https://developer.productboard.com/reference/getusers) |
| [List Custom Fields by Type](actions/list-custom-fields-by-type.md) | `GET /hierarchy-entities/custom-fields` | [docs](https://developer.productboard.com/reference/getcustomfields) |
