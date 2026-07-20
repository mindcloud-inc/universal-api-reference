# <img src="https://images.mindcloud.co/apps/icons/cryptlex_1774019059547.png" alt="Cryptlex logo" width="28" height="28"> Cryptlex: Universal API

Cryptlex is a software licensing and entitlement management platform for products, licenses, activations, releases, users, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cryptlex/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cryptlex.com
- **Vendor API docs:** https://api.cryptlex.com/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activation

| Action | Method | Description |
| --- | --- | --- |
| [Get Activation](actions/get-activation.md) | GET | Retrieves an activation from Cryptlex. |
| [List Activations](actions/list-activations.md) | GET | Retrieves activations from Cryptlex. |

### License

| Action | Method | Description |
| --- | --- | --- |
| [Create License](actions/create-license.md) | POST | Creates a license in Cryptlex. |
| [Extend License](actions/extend-license.md) | PUT | Extends a license in Cryptlex. |
| [Get License](actions/get-license.md) | GET | Retrieves a license from Cryptlex. |
| [List Licenses](actions/list-licenses.md) | GET | Retrieves licenses from Cryptlex. |
| [Renew License](actions/renew-license.md) | PUT | Renews a license in Cryptlex. |
| [Update License](actions/update-license.md) | PUT | Updates an existing license in Cryptlex. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Cryptlex. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Cryptlex. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Cryptlex. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Cryptlex. |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Create Release](actions/create-release.md) | POST | Creates a release in Cryptlex. |
| [Get Release](actions/get-release.md) | GET | Retrieves a release from Cryptlex. |
| [List Releases](actions/list-releases.md) | GET | Retrieves releases from Cryptlex. |
| [Publish Release](actions/publish-release.md) | PUT | Publishes a release in Cryptlex. |

### Release Platform

| Action | Method | Description |
| --- | --- | --- |
| [Create Release Platform](actions/create-release-platform.md) | POST | Creates a release platform in Cryptlex. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in Cryptlex. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Cryptlex. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Cryptlex. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Cryptlex. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Cryptlex. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Cryptlex. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Cryptlex. |

