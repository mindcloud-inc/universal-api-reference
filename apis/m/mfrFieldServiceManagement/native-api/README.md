# mfr Field Service Management: Native API Reference

A consolidated summary of mfr Field Service Management's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/6932380/2sB3dWsn6U
- **API base URL:** `https://portal.mobilefieldreport.com/odata`

## Authentication

### Basic Auth

Use an mfr portal username and password as documented in the official API documentation.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## API conventions

Responses from this API use JSON. Response data is read from `value`.

## Pagination

Use `$top` in the query string to set the page size (default 50; accepted range 1–200). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST Appointments` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Create Company](actions/create-company.md) | `POST Companies` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Create Contact](actions/create-contact.md) | `POST Contacts` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Create Service Object](actions/create-service-object.md) | `POST ServiceObjects` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Create Service Request](actions/create-service-request.md) | `POST ServiceRequests` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Delete Service Object](actions/delete-service-object.md) | `DELETE ServiceObjects({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Delete Service Request](actions/delete-service-request.md) | `DELETE ServiceRequests({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Find Company by ID](actions/find-company-by-id.md) | `GET Companies?$filter=Id eq {{id}}L` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Find Contact by ID](actions/find-contact-by-id.md) | `GET Contacts?$filter=Id eq {{id}}L` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Find Service Object by ID](actions/find-service-object-by-id.md) | `GET ServiceObjects?$filter=Id eq {{id}}L` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Find Service Request by ID](actions/find-service-request-by-id.md) | `GET ServiceRequests?$filter=Id eq {{id}}L` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Appointments](actions/list-appointments.md) | `GET Appointments` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Companies](actions/list-companies.md) | `GET Companies` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Contacts](actions/list-contacts.md) | `GET Contacts` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Service Objects](actions/list-service-objects.md) | `GET ServiceObjects` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Service Objects by Company](actions/list-service-objects-by-company.md) | `GET ServiceObjects?$filter=Company/Id eq {{companyId}}L` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Service Requests](actions/list-service-requests.md) | `GET ServiceRequests` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Service Requests by External ID](actions/list-service-requests-by-external-id.md) | `GET ServiceRequests?$filter=ExternalId eq '{{externalId}}'` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [List Time Events](actions/list-time-events.md) | `GET TimeEvents` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Update Appointment](actions/update-appointment.md) | `PUT Appointments({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Update Company](actions/update-company.md) | `PUT Companies({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Update Contact](actions/update-contact.md) | `PUT Contacts({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Update Service Object](actions/update-service-object.md) | `PUT ServiceObjects({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
| [Update Service Request](actions/update-service-request.md) | `PUT ServiceRequests({{id}}L)` | [docs](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U) |
