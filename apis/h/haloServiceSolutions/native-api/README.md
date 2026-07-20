# Halo Service Solutions: Native API Reference

A consolidated summary of Halo Service Solutions's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://usehalo.com/swagger/
- **API base URL:** `https://mindcloud.halopsa.com/api`

## Authentication

### OAuth 2.0

OAuth 2.0 Authorization Code for Halo tenant access

### Credentials

- **Base URL:** `baseUrl` · required · Halo tenant base URL, for example https://yourcompany.halopsa.com

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.baseUrl}}/auth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.baseUrl}}/auth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `all`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://usehalo.com/?guide=1-runbooks-authorising-api-access-into-your-own-halo-instance)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page_size` in the query string to set the page size. Use `page_no` in the query string to choose the page; numbering starts at 1.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | `POST /Actions` | [docs](https://usehalo.com/swagger/) |
| [Create Agent](actions/create-agent.md) | `POST /Agent` | [docs](https://usehalo.com/swagger/) |
| [Create Appointment](actions/create-appointment.md) | `POST /Appointment` | [docs](https://usehalo.com/swagger/) |
| [Create Asset](actions/create-asset.md) | `POST /Asset` | [docs](https://usehalo.com/swagger/) |
| [Create Client](actions/create-client.md) | `POST /Client` | [docs](https://usehalo.com/swagger/) |
| [Create Invoice](actions/create-invoice.md) | `POST /Invoice` | [docs](https://usehalo.com/swagger/) |
| [Create Project](actions/create-project.md) | `POST /Projects` | [docs](https://usehalo.com/swagger/) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /PurchaseOrder` | [docs](https://usehalo.com/swagger/) |
| [Create Quotation](actions/create-quotation.md) | `POST /Quotation` | [docs](https://usehalo.com/swagger/) |
| [Create Sales Order](actions/create-sales-order.md) | `POST /SalesOrder` | [docs](https://usehalo.com/swagger/) |
| [Create Site](actions/create-site.md) | `POST /Site` | [docs](https://usehalo.com/swagger/) |
| [Create Ticket](actions/create-ticket.md) | `POST /Tickets` | [docs](https://usehalo.com/swagger/) |
| [Create User](actions/create-user.md) | `POST /Users` | [docs](https://usehalo.com/swagger/) |
| [Get Action](actions/get-action.md) | `GET /Actions/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Agent](actions/get-agent.md) | `GET /Agent/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Appointment](actions/get-appointment.md) | `GET /Appointment/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Asset](actions/get-asset.md) | `GET /Asset/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Client](actions/get-client.md) | `GET /Client/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Current Agent](actions/get-current-agent.md) | `GET /Agent/me` | [docs](https://usehalo.com/swagger/) |
| [Get Invoice](actions/get-invoice.md) | `GET /Invoice/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Project](actions/get-project.md) | `GET /Projects/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /PurchaseOrder/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Quotation](actions/get-quotation.md) | `GET /Quotation/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /SalesOrder/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Site](actions/get-site.md) | `GET /Site/:id` | [docs](https://usehalo.com/swagger/) |
| [Get Ticket](actions/get-ticket.md) | `GET /Tickets/:id` | [docs](https://usehalo.com/swagger/) |
| [Get User](actions/get-user.md) | `GET /Users/:id` | [docs](https://usehalo.com/swagger/) |
| [List Actions](actions/list-actions.md) | `GET /Actions` | [docs](https://usehalo.com/swagger/) |
| [List Agents](actions/list-agents.md) | `GET /Agent` | [docs](https://usehalo.com/swagger/) |
| [List Appointments](actions/list-appointments.md) | `GET /Appointment` | [docs](https://usehalo.com/swagger/) |
| [List Assets](actions/list-assets.md) | `GET /Asset` | [docs](https://usehalo.com/swagger/) |
| [List Clients](actions/list-clients.md) | `GET /Client` | [docs](https://usehalo.com/swagger/) |
| [List Invoices](actions/list-invoices.md) | `GET /Invoice` | [docs](https://usehalo.com/swagger/) |
| [List Projects](actions/list-projects.md) | `GET /Projects` | [docs](https://usehalo.com/swagger/) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /PurchaseOrder` | [docs](https://usehalo.com/swagger/) |
| [List Quotations](actions/list-quotations.md) | `GET /Quotation` | [docs](https://usehalo.com/swagger/) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /SalesOrder` | [docs](https://usehalo.com/swagger/) |
| [List Sites](actions/list-sites.md) | `GET /Site` | [docs](https://usehalo.com/swagger/) |
| [List Tickets](actions/list-tickets.md) | `GET /Tickets` | [docs](https://usehalo.com/swagger/) |
| [List Users](actions/list-users.md) | `GET /Users` | [docs](https://usehalo.com/swagger/) |
| [View Tickets](actions/view-tickets.md) | `POST /Tickets/View` | [docs](https://usehalo.com/swagger/) |
