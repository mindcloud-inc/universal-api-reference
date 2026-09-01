# Amark: Native API Reference

A consolidated summary of Amark's API configuration and 14 documented operations.

- **API base URL:** `{environment}`

## Authentication

### OAuth 2.0 Client Credentials

Authenticate with Microsoft Entra ID using OAuth 2.0 Client Credentials.

### Credentials

- **Tenant ID:** `tenantId` · required · Microsoft Entra tenant GUID or verified tenant domain.
- **Application ID URI:** `applicationIdUri` · required · Resource Application ID URI used to request the /.default scope.
- **Environment:** `environment` · required · Choose Production or Sandbox. Production is selected by default.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/{{credentials.tenantId}}/oauth2/v2.0/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `api://5443830c-7ebd-4a64-a8af-c2630298e353/.default`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-client-creds-grant-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Products](actions/bulk-create-products.md) | `POST /Product/BulkCreate` |  |
| [Bulk Update Products](actions/bulk-update-products.md) | `POST /Product/BulkModify` |  |
| [Cancel Order](actions/cancel-order.md) | `POST /Order/Cancel` |  |
| [Create Order](actions/create-order.md) | `POST /Order/Create` |  |
| [Create Product](actions/create-product.md) | `POST /Product/Create` |  |
| [Create Receipt](actions/create-receipt.md) | `POST /Receipt/Create` |  |
| [Create Supplier](actions/create-supplier.md) | `POST /Supplier/Create` |  |
| [Get Order Info](actions/get-order-info.md) | `POST /Order/Info` | [docs](https://vaultlinkapi-sandbox.gold.com/) |
| [Get Product Info](actions/get-product-info.md) | `POST /Product/Info` |  |
| [Get Receipt Info](actions/get-receipt-info.md) | `POST /Receipt/Info` |  |
| [Get Supplier Info](actions/get-supplier-info.md) | `POST /Supplier/Info` |  |
| [Update Product](actions/update-product.md) | `POST /Product/Modify` |  |
| [Update Receipt](actions/update-receipt.md) | `POST /Receipt/Modify` |  |
| [Update Supplier](actions/update-supplier.md) | `POST /Supplier/Modify` |  |
