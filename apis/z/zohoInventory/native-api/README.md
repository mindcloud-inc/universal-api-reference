# Zoho Inventory: Native API Reference

A consolidated summary of Zoho Inventory's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/inventory/api/v1/introduction/
- **OpenAPI specification:** https://www.zoho.com/inventory/api/v1/openapi-all.zip
- **API base URL:** `{api_domain}/inventory/v1`

## Authentication

### OAuth 2.0

### Credentials

- **Organization ID:** `organizationId` · optional · Optional default Zoho Inventory organization_id. Run List Organizations after connecting, then save an organization_id where org_joined_app_list includes inventory.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoInventory.settings.READ,ZohoInventory.contacts.CREATE,ZohoInventory.contacts.READ,ZohoInventory.contacts.UPDATE,ZohoInventory.items.CREATE,ZohoInventory.items.READ,ZohoInventory.items.UPDATE,ZohoInventory.salesorders.CREATE,ZohoInventory.salesorders.READ,ZohoInventory.salesorders.UPDATE,ZohoInventory.packages.CREATE,ZohoInventory.packages.READ,ZohoInventory.shipmentorders.CREATE,ZohoInventory.shipmentorders.READ,ZohoInventory.shipmentorders.UPDATE,ZohoInventory.invoices.CREATE,ZohoInventory.invoices.READ,ZohoInventory.invoices.UPDATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/inventory/api/v1/oauth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The current page number is read from `page_context.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Sales Order](actions/confirm-sales-order.md) | `POST /salesorders/:salesorder_id/status/confirmed` | [docs](https://www.zoho.com/inventory/api/v1/salesorders/#mark-as-confirmed) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.zoho.com/inventory/api/v1/contacts/#create-a-contact) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.zoho.com/inventory/api/v1/invoices/#create-an-invoice) |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://www.zoho.com/inventory/api/v1/items/#create-an-item) |
| [Create Package](actions/create-package.md) | `POST /packages` | [docs](https://www.zoho.com/inventory/api/v1/packages/#creating-a-package) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /salesorders` | [docs](https://www.zoho.com/inventory/api/v1/salesorders/#create-a-sales-order) |
| [Create Shipment Order](actions/create-shipment-order.md) | `POST /shipmentorders` | [docs](https://www.zoho.com/inventory/api/v1/shipmentorders/#create-a-shipment-order) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://www.zoho.com/inventory/api/v1/contacts/#get-contact) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://www.zoho.com/inventory/api/v1/invoices/#get-an-invoice) |
| [Get Item](actions/get-item.md) | `GET /items/:item_id` | [docs](https://www.zoho.com/inventory/api/v1/items/#retrieve-an-item) |
| [Get Package](actions/get-package.md) | `GET /packages/:package_id` | [docs](https://www.zoho.com/inventory/api/v1/packages/#retrieving-a-package) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /salesorders/:salesorder_id` | [docs](https://www.zoho.com/inventory/api/v1/salesorders/#retrieve-a-sales-order) |
| [Get Shipment Order](actions/get-shipment-order.md) | `GET /shipmentorders/:shipmentorder_id` | [docs](https://www.zoho.com/inventory/api/v1/shipmentorders/#retrieve-a-shipment-order) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.zoho.com/inventory/api/v1/contacts/#list-contacts) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.zoho.com/inventory/api/v1/invoices/#list-invoices) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://www.zoho.com/inventory/api/v1/items/#list-all-the-items) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.zoho.com/inventory/api/v1/organizations/#list-organizations) |
| [List Packages](actions/list-packages.md) | `GET /packages` | [docs](https://www.zoho.com/inventory/api/v1/packages/#list-all-packages) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /salesorders` | [docs](https://www.zoho.com/inventory/api/v1/salesorders/#list-all-sales-orders) |
| [Mark Shipment Order Delivered](actions/mark-shipment-order-delivered.md) | `POST /shipmentorders/:shipmentorder_id/status/delivered` | [docs](https://www.zoho.com/inventory/api/v1/shipmentorders/#mark-as-delivered) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://www.zoho.com/inventory/api/v1/contacts/#update-a-contact) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://www.zoho.com/inventory/api/v1/invoices/#update-an-invoice) |
| [Update Item](actions/update-item.md) | `PUT /items/:item_id` | [docs](https://www.zoho.com/inventory/api/v1/items/#update-an-item) |
| [Update Sales Order](actions/update-sales-order.md) | `PUT /salesorders/:salesorder_id` | [docs](https://www.zoho.com/inventory/api/v1/salesorders/#update-a-sales-order) |
