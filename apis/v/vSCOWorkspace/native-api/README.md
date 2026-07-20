# VSCO Workspace: Native API Reference

A consolidated summary of VSCO Workspace's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://workspace.vsco.co/api
- **OpenAPI specification:** https://workspace.vsco.co/api/v2/openapi.json
- **API base URL:** `https://workspace.vsco.co/api/v2`

## Authentication

### API Key

Connect to VSCO Workspace with a Workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://help.workspace.vsco.co/en/articles/9146126-public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.totalPages`. The current page number is read from `meta.currentPage`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 10–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Payment to Order](actions/apply-payment-to-order.md) | `POST /payment/:id/apply` | [docs](https://workspace.vsco.co/api/#operation/createResourceApplyPaymentToOrder) |
| [Create Contact](actions/create-contact.md) | `POST /address-book` | [docs](https://workspace.vsco.co/api/#operation/createResourceAddressBook) |
| [Create Event](actions/create-event.md) | `POST /event` | [docs](https://workspace.vsco.co/api/#operation/createResourceEvent) |
| [Create File](actions/create-file.md) | `POST /file` | [docs](https://workspace.vsco.co/api/#operation/createResourceFile) |
| [Create Gallery](actions/create-gallery.md) | `POST /gallery` | [docs](https://workspace.vsco.co/api/#operation/createResourceGallery) |
| [Create Job](actions/create-job.md) | `POST /job` | [docs](https://workspace.vsco.co/api/#operation/createResourceJob) |
| [Create Order for Job](actions/create-order-for-job.md) | `POST /job/:jobId/order` | [docs](https://workspace.vsco.co/api/#operation/createResourceJobOrder) |
| [Create Payment](actions/create-payment.md) | `POST /payment` | [docs](https://workspace.vsco.co/api/#operation/createResourcePayment) |
| [Get Contact](actions/get-contact.md) | `GET /address-book/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceAddressBook) |
| [Get Event](actions/get-event.md) | `GET /event/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceEvent) |
| [Get File](actions/get-file.md) | `GET /file/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceFile) |
| [Get Gallery](actions/get-gallery.md) | `GET /gallery/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceGallery) |
| [Get Job](actions/get-job.md) | `GET /job/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceJob) |
| [Get My Studio](actions/get-my-studio.md) | `GET /studio/me` | [docs](https://workspace.vsco.co/api/#operation/getResourceMyStudio) |
| [Get Order](actions/get-order.md) | `GET /order/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourceOrder) |
| [Get Payment](actions/get-payment.md) | `GET /payment/:id` | [docs](https://workspace.vsco.co/api/#operation/getResourcePayment) |
| [List Contacts](actions/list-contacts.md) | `GET /address-book` | [docs](https://workspace.vsco.co/api/#operation/listResourceAddressBook) |
| [List Events](actions/list-events.md) | `GET /event` | [docs](https://workspace.vsco.co/api/#operation/listResourceEvent) |
| [List Files](actions/list-files.md) | `GET /file` | [docs](https://workspace.vsco.co/api/#operation/listResourceFile) |
| [List Galleries](actions/list-galleries.md) | `GET /gallery` | [docs](https://workspace.vsco.co/api/#operation/listResourceGallery) |
| [List Jobs](actions/list-jobs.md) | `GET /job` | [docs](https://workspace.vsco.co/api/#operation/listResourceJob) |
| [List Orders](actions/list-orders.md) | `GET /order` | [docs](https://workspace.vsco.co/api/#operation/listResourceOrder) |
| [List Orders for Job](actions/list-orders-for-job.md) | `GET /job/:jobId/order` | [docs](https://workspace.vsco.co/api/#operation/listResourceJobOrders) |
| [List Payments](actions/list-payments.md) | `GET /payment` | [docs](https://workspace.vsco.co/api/#operation/listResourcePayment) |
| [List Payments for Job](actions/list-payments-for-job.md) | `GET /job/:id/payment` | [docs](https://workspace.vsco.co/api/#operation/listResourceJobPayment) |
| [Update Contact](actions/update-contact.md) | `PUT /address-book/:id` | [docs](https://workspace.vsco.co/api/#operation/updateResourceAddressBook) |
| [Update Event](actions/update-event.md) | `PUT /event/:id` | [docs](https://workspace.vsco.co/api/#operation/updateResourceEvent) |
| [Update Gallery](actions/update-gallery.md) | `PUT /gallery/:id` | [docs](https://workspace.vsco.co/api/#operation/updateResourceGallery) |
| [Update Job](actions/update-job.md) | `PUT /job/:id` | [docs](https://workspace.vsco.co/api/#operation/updateResourceJob) |
| [Update Order](actions/update-order.md) | `PUT /order/:id` | [docs](https://workspace.vsco.co/api/#operation/updateResourceOrder) |
