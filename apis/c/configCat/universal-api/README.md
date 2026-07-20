# <img src="https://images.mindcloud.co/apps/icons/favicon-5_1774987007808.png" alt="ConfigCat logo" width="28" height="28"> ConfigCat: Universal API

Manage feature flags, configs, environments, and products in ConfigCat

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/configCat/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://configcat.com/
- **Vendor API docs:** https://configcat.com/docs/api/reference/configcat-public-management-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User Details](actions/get-authenticated-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/get-authenticated-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Authenticated User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User Details](actions/get-authenticated-user-details.md) | GET | Retrieves authenticated user details from ConfigCat. |

### Config

| Action | Method | Description |
| --- | --- | --- |
| [Create Config](actions/create-config.md) | POST | Creates a new config in ConfigCat. |
| [Delete Config](actions/delete-config.md) | DELETE | Deletes an existing config from ConfigCat. |
| [Get Config](actions/get-config.md) | GET | Retrieves an existing config from ConfigCat. |
| [List Configs](actions/list-configs.md) | GET | Retrieves configs from a ConfigCat product. |
| [Update Config](actions/update-config.md) | PUT | Updates an existing config in ConfigCat. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in ConfigCat. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from ConfigCat. |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an existing environment from ConfigCat. |
| [List Environments](actions/list-environments.md) | GET | Retrieves a list of environments from ConfigCat. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in ConfigCat. |

### Flag

| Action | Method | Description |
| --- | --- | --- |
| [Create Flag](actions/create-flag.md) | POST | Creates a new flag in ConfigCat. |
| [Delete Flag](actions/delete-flag.md) | DELETE | Deletes an existing flag from ConfigCat. |
| [List Flags](actions/list-flags.md) | GET | Retrieves flags from a ConfigCat config. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from ConfigCat. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in ConfigCat. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from ConfigCat. |
| [Get Product](actions/get-product.md) | GET | Retrieves an existing product from ConfigCat. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from ConfigCat. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in ConfigCat. |

