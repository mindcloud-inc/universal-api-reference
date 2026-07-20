# Zoho Billing: Native API Reference

A consolidated summary of Zoho Billing's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/billing/api/v1/introduction/
- **OpenAPI specification:** https://www.zoho.com/billing/api/v1/openapi-all.zip
- **API base URL:** `{api_domain}/billing/v1`

## Authentication

### OAuth 2.0

### Credentials

- **Organization ID:** `organizationId` · required · This app requires a Zoho Organization ID. Choose the organization you want to work with before connecting.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoSubscriptions.settings.READ,ZohoSubscriptions.products.CREATE,ZohoSubscriptions.products.READ,ZohoSubscriptions.products.UPDATE,ZohoSubscriptions.plans.CREATE,ZohoSubscriptions.plans.READ,ZohoSubscriptions.plans.UPDATE,ZohoSubscriptions.customers.CREATE,ZohoSubscriptions.customers.READ,ZohoSubscriptions.customers.UPDATE,ZohoSubscriptions.subscriptions.CREATE,ZohoSubscriptions.subscriptions.READ,ZohoSubscriptions.subscriptions.UPDATE,ZohoSubscriptions.invoices.CREATE,ZohoSubscriptions.invoices.READ,ZohoSubscriptions.invoices.UPDATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/billing/api/v1/oauth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /subscriptions/:subscription_id/cancel` | [docs](https://www.zoho.com/billing/api/v1/subscription/#cancel-a-subscription) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://www.zoho.com/billing/api/v1/customers/#create-a-customer) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.zoho.com/billing/api/v1/invoices/#create-an-invoice) |
| [Create Plan](actions/create-plan.md) | `POST /plans` | [docs](https://www.zoho.com/billing/api/v1/plans/#create-a-plan) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://www.zoho.com/billing/api/v1/products/#create-a-product) |
| [Create Subscription](actions/create-subscription.md) | `POST /subscriptions` | [docs](https://www.zoho.com/billing/api/v1/subscription/#create-a-subscription) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization_id` | [docs](https://www.zoho.com/billing/api/v1/organizations/#get-an-organization) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.zoho.com/billing/api/v1/customers/#list-all-customers) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.zoho.com/billing/api/v1/invoices/#list-all-invoices) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.zoho.com/billing/api/v1/organizations/#list-organizations) |
| [List Plans](actions/list-plans.md) | `GET /plans` | [docs](https://www.zoho.com/billing/api/v1/plans/#list-all-plans) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://www.zoho.com/billing/api/v1/products/#list-of-all-products) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://www.zoho.com/billing/api/v1/subscription/#list-all-subscriptions) |
| [Reactivate Subscription](actions/reactivate-subscription.md) | `POST /subscriptions/:subscription_id/reactivate` | [docs](https://www.zoho.com/billing/api/v1/subscription/#reactivate-subscription) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:customer_id` | [docs](https://www.zoho.com/billing/api/v1/customers/#retrieve-a-customer) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://www.zoho.com/billing/api/v1/invoices/#retrieve-an-invoice) |
| [Retrieve Plan](actions/retrieve-plan.md) | `GET /plans/:plan_code` | [docs](https://www.zoho.com/billing/api/v1/plans/#retrieve-a-plan) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /products/:product_id` | [docs](https://www.zoho.com/billing/api/v1/products/#retrieve-a-product) |
| [Retrieve Subscription](actions/retrieve-subscription.md) | `GET /subscriptions/:subscription_id` | [docs](https://www.zoho.com/billing/api/v1/subscription/#retrieve-a-subscription) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customer_id` | [docs](https://www.zoho.com/billing/api/v1/customers/#update-a-customer) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://www.zoho.com/billing/api/v1/invoices/#update-an-invoice) |
| [Update Plan](actions/update-plan.md) | `PUT /plans/:plan_code` | [docs](https://www.zoho.com/billing/api/v1/plans/#update-a-plan) |
| [Update Product](actions/update-product.md) | `PUT /products/:product_id` | [docs](https://www.zoho.com/billing/api/v1/products/#update-a-product) |
| [Update Subscription](actions/update-subscription.md) | `PUT /subscriptions/:subscription_id` | [docs](https://www.zoho.com/billing/api/v1/subscription/#update-a-subscription) |
