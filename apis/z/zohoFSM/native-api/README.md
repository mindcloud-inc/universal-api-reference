# Zoho FSM: Native API Reference

A consolidated summary of Zoho FSM's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/fsm/developer/help/api/
- **API base URL:** `{api_domain}/fsm/v1`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoFSM.modules.Requests.READ ZohoFSM.modules.Requests.CREATE ZohoFSM.modules.Requests.UPDATE ZohoFSM.modules.WorkOrders.READ ZohoFSM.modules.WorkOrders.CREATE ZohoFSM.modules.WorkOrders.UPDATE ZohoFSM.modules.ServiceAppointments.READ ZohoFSM.modules.ServiceAppointments.CREATE ZohoFSM.modules.ServiceAppointments.UPDATE ZohoFSM.modules.Contacts.READ ZohoFSM.modules.Contacts.CREATE ZohoFSM.modules.Companies.READ ZohoFSM.modules.Companies.CREATE ZohoFSM.modules.Estimates.READ ZohoFSM.modules.Estimates.CREATE ZohoFSM.modules.Service_And_Parts.READ ZohoFSM.modules.Service_And_Parts.CREATE`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/fsm/developer/help/api/oauth-overview.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /Companies` | [docs](https://www.zoho.com/fsm/developer/help/api/create-company.html) |
| [Create Contact](actions/create-contact.md) | `POST /Contacts` | [docs](https://www.zoho.com/fsm/developer/help/api/create-contact.html) |
| [Create Estimate](actions/create-estimate.md) | `POST /Estimates` | [docs](https://www.zoho.com/fsm/developer/help/api/create-estimate.html) |
| [Create Request](actions/create-request.md) | `POST /Requests` | [docs](https://www.zoho.com/fsm/developer/help/api/create-request.html) |
| [Create Service Appointment](actions/create-service-appointment.md) | `POST /Service_Appointments` | [docs](https://www.zoho.com/fsm/developer/help/api/create-service-appointment.html) |
| [Create Work Order](actions/create-work-order.md) | `POST /Work_Orders` | [docs](https://www.zoho.com/fsm/developer/help/api/create-work-order.html) |
| [Get Company](actions/get-company.md) | `GET /Companies/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/get-a-company.html) |
| [Get Contact](actions/get-contact.md) | `GET /Contacts/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/get-a-contact.html) |
| [Get Estimate](actions/get-estimate.md) | `GET /Estimates/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/get-an-estimate.html) |
| [Get Request](actions/get-request.md) | `GET /Requests/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/get-a-request.html) |
| [Get Work Order](actions/get-work-order.md) | `GET /Work_Orders/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/get-a-work-order.html) |
| [List Companies](actions/list-companies.md) | `GET /Companies` | [docs](https://www.zoho.com/fsm/developer/help/api/get-companies.html) |
| [List Contacts](actions/list-contacts.md) | `GET /Contacts` | [docs](https://www.zoho.com/fsm/developer/help/api/get-contacts.html) |
| [List Estimates](actions/list-estimates.md) | `GET /Estimates` | [docs](https://www.zoho.com/fsm/developer/help/api/get-estimates.html) |
| [List Request Transitions](actions/list-request-transitions.md) | `GET /Requests/:recordId/actions/blueprint/transitions` | [docs](https://www.zoho.com/fsm/developer/help/api/list-request-transitions.html) |
| [List Requests](actions/list-requests.md) | `GET /Requests` | [docs](https://www.zoho.com/fsm/developer/help/api/get-requests.html) |
| [List Service Appointments](actions/list-service-appointments.md) | `GET /Service_Appointments` | [docs](https://www.zoho.com/fsm/developer/help/api/get-service-appointments.html) |
| [List Work Order Transitions](actions/list-work-order-transitions.md) | `GET /Work_Orders/:recordId/actions/blueprint/transitions` | [docs](https://www.zoho.com/fsm/developer/help/api/list-work-order-transitions.html) |
| [List Work Orders](actions/list-work-orders.md) | `GET /Work_Orders` | [docs](https://www.zoho.com/fsm/developer/help/api/get-work-orders.html) |
| [Perform Request Transition](actions/perform-request-transition.md) | `PUT /Requests/:recordId/actions/blueprint` | [docs](https://www.zoho.com/fsm/developer/help/api/perform-request-transition.html) |
| [Perform Work Order Transition](actions/perform-work-order-transition.md) | `PUT /Work_Orders/:recordId/actions/blueprint` | [docs](https://www.zoho.com/fsm/developer/help/api/perform-work-order-transition.html) |
| [Update Request](actions/update-request.md) | `PUT /Requests/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/edit-request.html) |
| [Update Service Appointment](actions/update-service-appointment.md) | `PUT /Service_Appointments` | [docs](https://www.zoho.com/fsm/developer/help/api/edit-service-appointment.html) |
| [Update Work Order](actions/update-work-order.md) | `PUT /Work_Orders/:recordId` | [docs](https://www.zoho.com/fsm/developer/help/api/edit-work-order.html) |
