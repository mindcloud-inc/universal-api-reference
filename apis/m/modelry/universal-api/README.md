# <img src="https://images.mindcloud.co/apps/icons/634d09b45cb8ac2828065962-modelry-logo_1776278919173.png" alt="Modelry logo" width="28" height="28"> Modelry: Universal API

Manage product assets, modeling requests, and embeds

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/modelry/latest
- **Category:** Commerce
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.modelry.ai
- **Vendor API docs:** https://files.cgtarsenal.com/api/doc/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Asset](actions/create-product-asset.md) | POST |  |
| [Delete Product Asset](actions/delete-product-asset.md) | DELETE |  |
| [Download Product Assets](actions/download-product-assets.md) | GET |  |

### Embed

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Embed](actions/create-product-embed.md) | POST |  |
| [Delete Product Embed](actions/delete-product-embed.md) | DELETE |  |
| [Get Product Embed](actions/get-product-embed.md) | GET |  |
| [List Product Embeds](actions/list-product-embeds.md) | GET |  |
| [Publish Product Embed](actions/publish-product-embed.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Blob](actions/create-blob.md) | POST |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Modeling Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Modeling Request](actions/create-modeling-request.md) | POST |  |
| [List Modeling Requests](actions/list-modeling-requests.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET |  |

