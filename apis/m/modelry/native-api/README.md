# Modelry: Native API Reference

A consolidated summary of Modelry's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://files.cgtarsenal.com/api/doc/index.html
- **API base URL:** `https://api.modelry.ai/api`

## Authentication

### API Key

Use a Modelry API token from Settings in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.modelry.ai/hc/en-us/articles/4949823833105-Do-you-offer-an-external-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `meta.total_pages`. The current page number is read from `meta.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Blob](actions/create-blob.md) | `POST /v1/blobs` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Uploads-Blobs) |
| [Create Modeling Request](actions/create-modeling-request.md) | `POST /v1/modeling-requests` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ModelingRequests-CreateModelingRequest) |
| [Create Product](actions/create-product.md) | `POST /v1/products` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Products-CreateProduct) |
| [Create Product Asset](actions/create-product-asset.md) | `POST /v1/products/:product_id/assets` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-CreateProductAsset) |
| [Create Product Embed](actions/create-product-embed.md) | `POST /v1/products/:product_id/embeds` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-CreateProductViewer) |
| [Delete Product](actions/delete-product.md) | `DELETE /v1/products/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Products-DeleteProduct) |
| [Delete Product Asset](actions/delete-product-asset.md) | `DELETE /v1/products/:product_id/assets/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-DeleteProductAsset) |
| [Delete Product Embed](actions/delete-product-embed.md) | `DELETE /v1/products/:product_id/embeds/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-DeleteProductViewer) |
| [Download Product Assets](actions/download-product-assets.md) | `GET /v1/products/:product_id/assets/download` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductAssets-DownloadProductAssets) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Products-GetProduct) |
| [Get Product Embed](actions/get-product-embed.md) | `GET /v1/products/:product_id/embeds/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-GetProductViewer) |
| [List Modeling Requests](actions/list-modeling-requests.md) | `GET /v1/modeling-requests` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ModelingRequests-GetModelingRequests) |
| [List Product Embeds](actions/list-product-embeds.md) | `GET /v1/products/:product_id/embeds` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-GetProductViewers) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Products-GetProducts) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Workspaces-GetWorkspaces) |
| [Publish Product Embed](actions/publish-product-embed.md) | `PUT /v1/products/:product_id/embeds/:id/publish` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-ProductViewers-PublishProductViewer) |
| [Update Product](actions/update-product.md) | `PUT /v1/products/:id` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Products-UpdateProduct) |
| [Upload File](actions/upload-file.md) | `POST /v1/uploads` | [docs](https://files.cgtarsenal.com/api/doc/index.html#api-Uploads-UploadFile) |
