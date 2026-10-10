# PestPac: Native API Reference

A consolidated summary of PestPac's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developer.workwave.com/documentation#pestpac
- **API base URL:** `https://api.workwave.com/pestpac/v1/`

## Authentication

### Custom

### Credentials

- **Username:** `username` · optional
- **Password:** `password` · optional
- **API Key:** `apiKey` · optional
- **Tenant ID:** `tenantId` · optional
- **Client Id:** `clientId` · optional
- **Client Secret:** `clientSecret` · optional

Send these headers with each API request:

```http
apiKey: <apiKey>
tenant-id: <tenantId>
Authorization: Bearer <custom.accessToken>
Authorization: Bearer <basicAuth>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Pagination

Use `skip` in the query string to set the page size (default 500; accepted range 500–500). Use `skip` in the query string as the record offset.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [CompanySetup](actions/company-setup.md) | `GET CompanySetup` |  |
| [Create Contact](actions/create-contact.md) | `POST Contacts` | [docs](https://developer.workwave.com/documentation) |
| [Create Document](actions/create-document.md) | `POST Documents` | [docs](https://developer.workwave.com/documentation) |
| [Create Location](actions/create-location.md) | `POST Locations` | [docs](https://developer.workwave.com/documentation) |
| [Create Payment](actions/create-payment.md) | `POST Payments` |  |
| [Get Access Token](actions/get-access-token.md) | `POST https://is.workwave.com/oauth2/token` |  |
| [Get Activity Log](actions/get-activity-log.md) | `GET activityLog` |  |
| [Get Bill](actions/get-bill.md) | `GET BillTos` |  |
| [Get Documents by Location ID](actions/get-documents-by-location-id.md) | `GET Locations/:locationId/documents` | [docs](https://developer.workwave.com/documentation) |
| [Get Invoices](actions/get-invoices.md) | `GET Invoices` |  |
| [Get Locations](actions/get-locations.md) | `GET Locations` |  |
| [Get Service Orders](actions/get-orders.md) | `GET ServiceOrders` |  |
| [Get Payment History By BillToId](actions/get-payment-history-by-bill-to-id.md) | `GET BillTos/:id/payments` |  |
| [Get Payments](actions/get-payments.md) | `GET Payments` |  |
| [Get Service Order Attributes](actions/get-service-order-attributes.md) | `GET ServiceOrders/:orderId/attributes` |  |
| [Get Service Orders by id](actions/get-service-orders-by-id.md) | `GET ServiceOrders/:id` |  |
| [Get Service Setups](actions/get-service-setups.md) | `GET ServiceSetups/:id` |  |
| [Get Services](actions/get-services.md) | `GET lookup/service` |  |
| [Get Test](actions/get-test.md) | `GET invoices?status=active` |  |
| [Leads](actions/leads.md) | `GET Leads` |  |
| [List Contacts](actions/list-contacts.md) | `GET Contacts` |  |
| [List Contacts by Location Id](actions/list-contacts-by-location-id.md) | `GET Locations/{{locationId}}/contacts` |  |
| [List Employees](actions/list-employees.md) | `GET lookups/Employees` |  |
| [List Invoices by ID](actions/list-invoices-by-id.md) | `GET Invoices/:id` |  |
| [List Location IDs](actions/list-location-i-ds.md) | `GET Locations/LocationIDList` |  |
| [List Schedules](actions/list-schedules.md) | `GET lookups/Schedules` |  |
| [List Service Orders](actions/list-service-orders.md) | `GET ServiceOrders` |  |
| [List Service Orders by Location ID](actions/list-service-orders-by-location-id.md) | `GET /Locations/:id/serviceOrders` |  |
| [List Service Setups by Location ID](actions/list-service-setups-by-location-id.md) | `GET /Locations/:id/ServiceSetups` |  |
| [List Unpaid Invoices by Location Id](actions/list-unpaid-invoices-by-location-id.md) | `GET Locations/:locationId/unpaidInvoices` |  |
| [Lookups](actions/lookups.md) | `GET /lookups/:lookupKey` |  |
| [Update Contact](actions/update-contact.md) | `PUT Contacts/:contactId` | [docs](https://developer.workwave.com/documentation) |
| [Update Document](actions/update-document.md) | `PUT Documents/:documentId` | [docs](https://developer.workwave.com/documentation) |
| [Update Location](actions/update-location.md) | `PUT Locations/:locationId` | [docs](https://developer.workwave.com/documentation) |
| [Update Webhook](actions/update-webhook.md) | `PUT WebHooks/:id` |  |
| [Upload Document](actions/upload-document.md) | `POST Documents/:documentId/upload` | [docs](https://developer.workwave.com/documentation) |
| [UserDefFields](actions/user-def-fields.md) | `GET UserDefFields` |  |
| [Get Webhooks](actions/web-hooks.md) | `GET WebHooks` |  |
