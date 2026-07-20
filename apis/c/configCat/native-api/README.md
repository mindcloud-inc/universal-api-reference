# ConfigCat: Native API Reference

A consolidated summary of ConfigCat's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://configcat.com/docs/api/reference/configcat-public-management-api/
- **OpenAPI specification:** https://api.configcat.com/docs/v1/swagger.json
- **API base URL:** `https://api.configcat.com`

## Authentication

### Basic Authentication

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://configcat.com/docs/api/reference/configcat-public-management-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Config](actions/create-config.md) | `POST /v1/products/:productId/configs` | [docs](https://configcat.com/docs/api/reference/create-config/) |
| [Create Environment](actions/create-environment.md) | `POST /v1/products/:productId/environments` | [docs](https://configcat.com/docs/api/reference/create-environment/) |
| [Create Flag](actions/create-flag.md) | `POST /v1/configs/:configId/settings` | [docs](https://configcat.com/docs/api/reference/create-setting/) |
| [Create Product](actions/create-product.md) | `POST /v1/organizations/:organizationId/products` | [docs](https://configcat.com/docs/api/reference/create-product/) |
| [Delete Config](actions/delete-config.md) | `DELETE /v1/configs/:configId` | [docs](https://configcat.com/docs/api/reference/delete-config/) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /v1/environments/:environmentId` | [docs](https://configcat.com/docs/api/reference/delete-environment/) |
| [Delete Flag](actions/delete-flag.md) | `DELETE /v1/settings/:settingId` | [docs](https://configcat.com/docs/api/reference/delete-setting/) |
| [Delete Product](actions/delete-product.md) | `DELETE /v1/products/:productId` | [docs](https://configcat.com/docs/api/reference/delete-product/) |
| [Get Authenticated User Details](actions/get-authenticated-user-details.md) | `GET /v1/me` | [docs](https://configcat.com/docs/api/reference/get-me/) |
| [Get Config](actions/get-config.md) | `GET /v1/configs/:configId` | [docs](https://configcat.com/docs/api/reference/get-config/) |
| [Get Environment](actions/get-environment.md) | `GET /v1/environments/:environmentId` | [docs](https://configcat.com/docs/api/reference/get-environment/) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:productId` | [docs](https://configcat.com/docs/api/reference/get-product/) |
| [List Configs](actions/list-configs.md) | `GET /v1/products/:productId/configs` | [docs](https://configcat.com/docs/api/reference/get-configs/) |
| [List Environments](actions/list-environments.md) | `GET /v1/products/:productId/environments` | [docs](https://configcat.com/docs/api/reference/get-environments/) |
| [List Flags](actions/list-flags.md) | `GET /v1/configs/:configId/settings` | [docs](https://configcat.com/docs/api/reference/get-settings/) |
| [List Organizations](actions/list-organizations.md) | `GET /v1/organizations` | [docs](https://configcat.com/docs/api/reference/get-organizations/) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://configcat.com/docs/api/reference/get-products/) |
| [Update Config](actions/update-config.md) | `PUT /v1/configs/:configId` | [docs](https://configcat.com/docs/api/reference/update-config/) |
| [Update Environment](actions/update-environment.md) | `PUT /v1/environments/:environmentId` | [docs](https://configcat.com/docs/api/reference/update-environment/) |
| [Update Product](actions/update-product.md) | `PUT /v1/products/:productId` | [docs](https://configcat.com/docs/api/reference/update-product/) |
