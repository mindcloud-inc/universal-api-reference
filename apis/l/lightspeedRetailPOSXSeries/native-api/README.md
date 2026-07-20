# Lightspeed Retail POS (X-Series): Native API Reference

A consolidated summary of Lightspeed Retail POS (X-Series)'s API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://x-series-api.lightspeedhq.com/docs/introduction
- **OpenAPI specification:** https://x-series-api.lightspeedhq.com/openapi/api-2026-04.yaml
- **API base URL:** `https://{domain_prefix}.retail.lightspeed.app`

## Authentication

### OAuth 2.0

Connect a retailer account using Lightspeed Retail (X-Series) OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://secure.retail.lightspeed.app/connect to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app/api/1.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `retailer:read users:read outlets:read registers:read sales:read customers:read customers:write products:read products:write inventory:read suppliers:read suppliers:write webhooks`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app/api/1.0/token.

[Official authentication documentation](https://x-series-api.lightspeedhq.com/docs/authorization)

## API conventions

Response data is read from `data`.

## Pagination

Use `after` in the query string as the pagination cursor.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /api/2.0/customers` | [docs](https://x-series-api.lightspeedhq.com/reference/createcustomer) |
| [Create Product](actions/create-product.md) | `POST /api/2.0/products` | [docs](https://x-series-api.lightspeedhq.com/reference/createproduct) |
| [Create Supplier](actions/create-supplier.md) | `POST /api/2.0/suppliers` | [docs](https://x-series-api.lightspeedhq.com/reference/createsupplier) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/2.0/webhooks` | [docs](https://x-series-api.lightspeedhq.com/reference/post-webhooks) |
| [Get Current User](actions/get-current-user.md) | `GET /api/2.0/user` | [docs](https://x-series-api.lightspeedhq.com/reference/getuser) |
| [Get Customer](actions/get-customer.md) | `GET /api/2.0/customers/:customer_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getcustomerbyid) |
| [Get Outlet](actions/get-outlet.md) | `GET /api/2.0/outlets/:outlet_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getoutletbyid) |
| [Get Product](actions/get-product.md) | `GET /api/2.0/products/:product_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getproductbyid) |
| [Get Register](actions/get-register.md) | `GET /api/2.0/registers/:register_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getregisterbyid) |
| [Get Retailer](actions/get-retailer.md) | `GET /api/2026-04/retailer` | [docs](https://x-series-api.lightspeedhq.com/reference/getretailer) |
| [Get Supplier](actions/get-supplier.md) | `GET /api/2.0/suppliers/:supplier_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getsupplierbyid) |
| [Get User](actions/get-user.md) | `GET /api/2.0/users/:user_id` | [docs](https://x-series-api.lightspeedhq.com/reference/getuserbyid) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/2.0/webhooks/:webhookId` | [docs](https://x-series-api.lightspeedhq.com/reference/get-webhooks-id) |
| [List Customers](actions/list-customers.md) | `GET /api/2.0/customers` | [docs](https://x-series-api.lightspeedhq.com/reference/listcustomers) |
| [List Outlets](actions/list-outlets.md) | `GET /api/2.0/outlets` | [docs](https://x-series-api.lightspeedhq.com/reference/listoutlets) |
| [List Products](actions/list-products.md) | `GET /api/2.0/products` | [docs](https://x-series-api.lightspeedhq.com/reference/listproducts) |
| [List Registers](actions/list-registers.md) | `GET /api/2.0/registers` | [docs](https://x-series-api.lightspeedhq.com/reference/listregisters) |
| [List Sales](actions/list-sales.md) | `GET /api/2.0/sales` | [docs](https://x-series-api.lightspeedhq.com/reference/listsales) |
| [List Suppliers](actions/list-suppliers.md) | `GET /api/2.0/suppliers` | [docs](https://x-series-api.lightspeedhq.com/reference/listsuppliers) |
| [List Users](actions/list-users.md) | `GET /api/2.0/users` | [docs](https://x-series-api.lightspeedhq.com/reference/listusers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/2.0/webhooks` | [docs](https://x-series-api.lightspeedhq.com/reference/get-webhooks) |
| [Update Customer](actions/update-customer.md) | `PUT /api/2.0/customers/:customer_id` | [docs](https://x-series-api.lightspeedhq.com/reference/updatecustomerbyid) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/2.0/webhooks/:webhookId` | [docs](https://x-series-api.lightspeedhq.com/reference/put-webhooks-id) |
