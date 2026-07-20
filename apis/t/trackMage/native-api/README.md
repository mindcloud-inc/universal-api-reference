# TrackMage: Native API Reference

A consolidated summary of TrackMage's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.trackmage.com/docs/
- **OpenAPI specification:** https://api.trackmage.com/docs?format=json
- **API base URL:** `https://api.trackmage.com/`

## Authentication

### OAuth2 Client Credentials

Connect TrackMage with OAuth2 client credentials. TrackMage also documents authorization-code OAuth, but this wrapper is frozen to the client-credentials path for this one-shot run.

### Credentials

- **Client ID:** `clientId` · required · The TrackMage OAuth client ID generated from Settings > API KEYS.
- **Client Secret:** `clientSecret` · required · The TrackMage OAuth client secret generated from Settings > API KEYS.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.trackmage.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a GET request to https://api.trackmage.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.trackmage.com/docs/authorization)

## API conventions

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://docs.trackmage.com/docs/product/product.html) |
| [Create Product Variant](actions/create-product-variant.md) | `POST /product_variants` | [docs](https://docs.trackmage.com/docs/product/product-variant.html) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Create Shipment Item](actions/create-shipment-item.md) | `POST /shipment_items` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://docs.trackmage.com/docs/workflow/workflow.html) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://docs.trackmage.com/docs/workspaces.html) |
| [Delete Order](actions/delete-order.md) | `DELETE /orders/{id}` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{id}` | [docs](https://docs.trackmage.com/docs/product/product.html) |
| [Delete Product Variant](actions/delete-product-variant.md) | `DELETE /product_variants/{id}` | [docs](https://docs.trackmage.com/docs/product/product-variant.html) |
| [Delete Shipment](actions/delete-shipment.md) | `DELETE /shipments/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Delete Shipment Item](actions/delete-shipment-item.md) | `DELETE /shipment_items/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /workspaces/{id}` | [docs](https://docs.trackmage.com/docs/workspaces.html) |
| [Execute Workflow](actions/execute-workflow.md) | `POST /workflows/execute` | [docs](https://docs.trackmage.com/docs/workflow/workflow.html) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://docs.trackmage.com/docs/product/product.html) |
| [Get Product Variant](actions/get-product-variant.md) | `GET /product_variants/{id}` | [docs](https://docs.trackmage.com/docs/product/product-variant.html) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Get Shipment Item](actions/get-shipment-item.md) | `GET /shipment_items/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/{id}` | [docs](https://docs.trackmage.com/docs/workflow/workflow.html) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/{id}` | [docs](https://docs.trackmage.com/docs/workspaces.html) |
| [List Order Items For Order](actions/list-order-items-for-order.md) | `GET /orders/{id}/items` | [docs](https://docs.trackmage.com/docs/order/order-item.html) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [List Product Variants](actions/list-product-variants.md) | `GET /product_variants` | [docs](https://docs.trackmage.com/docs/product/product-variant.html) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.trackmage.com/docs/product/product.html) |
| [List Shipment Checkpoints](actions/list-shipment-checkpoints.md) | `GET /shipments/{id}/checkpoints` | [docs](https://docs.trackmage.com/docs/shipment/tracking-checkpoint.html) |
| [List Shipment Items](actions/list-shipment-items.md) | `GET /shipment_items` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [List Shipment Items For Shipment](actions/list-shipment-items-for-shipment.md) | `GET /shipments/{id}/shipment_items` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://docs.trackmage.com/docs/workflow/workflow.html) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://docs.trackmage.com/docs/workspaces.html) |
| [Lookup Order](actions/lookup-order.md) | `POST /orders/lookup` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [Lookup Shipment](actions/lookup-shipment.md) | `POST /shipments/lookup` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Merge Shipments](actions/merge-shipments.md) | `POST /shipments/merge` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Update Order](actions/update-order.md) | `PUT /orders/{id}` | [docs](https://docs.trackmage.com/docs/order/order.html) |
| [Update Product](actions/update-product.md) | `PUT /products/{id}` | [docs](https://docs.trackmage.com/docs/product/product.html) |
| [Update Product Variant](actions/update-product-variant.md) | `PUT /product_variants/{id}` | [docs](https://docs.trackmage.com/docs/product/product-variant.html) |
| [Update Shipment](actions/update-shipment.md) | `PUT /shipments/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment.html) |
| [Update Shipment Item](actions/update-shipment-item.md) | `PUT /shipment_items/{id}` | [docs](https://docs.trackmage.com/docs/shipment/shipment-item.html) |
| [Update Workspace](actions/update-workspace.md) | `PUT /workspaces/{id}` | [docs](https://docs.trackmage.com/docs/workspaces.html) |
