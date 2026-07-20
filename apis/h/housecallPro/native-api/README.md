# Housecall Pro: Native API Reference

A consolidated summary of Housecall Pro's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.housecallpro.com/docs/housecall-public-api/a4ca20a18010c-housecall-v1-api
- **API base URL:** `https://api.housecallpro.com`

## Authentication

### API Key

Connect with a Housecall Pro API key generated from the Housecall Pro App Store API card.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.housecallpro.com/docs/housecall-public-api/docs/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `total_pages`. The current page number is read from `page`.

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Estimate Option Line Items](actions/bulk-update-estimate-option-line-items.md) | `PUT /estimates/:estimate_id/options/:option_id/line_items/bulk_update` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/b3e4391f7853f) |
| [Convert Lead to Estimate or Job](actions/convert-lead-to-estimate-or-job.md) | `POST /leads/:id/convert` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/d9c8a89ed4e4c-convert-lead-to-estimate-or-job) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/4e0bf8c4d65d7-create-customer) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/4004d373be14c) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/2dcf481ed7d69-create-a-job) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/8961eaf9f1c28-create-lead) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/24a5d891a80a8-get-company) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customer_id` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/7599b1ec89338-get-customer) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:estimate_id` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/eae5e9c092ef2) |
| [Get Invoice](actions/get-invoice.md) | `GET /api/invoices/:uuid` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/0ae16219c3e58) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/bbabd67bed1ab-get-a-job) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:id` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/fc11c266161fe-get-lead) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/042bd3bf861ae-get-customers) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/303ee235f23fa-get-employees) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/e430ba3d520a0) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/65ce9f430d605) |
| [List Job Invoices](actions/list-job-invoices.md) | `GET /jobs/:job_id/invoices` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/eb1f5b5f17290) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/6c97704da8bf3-get-jobs) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/278974bc87e32-get-leads) |
| [Preview Invoice by UUID](actions/preview-invoice-by-uuid.md) | `GET /api/invoices/:uuid/preview` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/ae40a9286ba7c) |
| [Schedule Windows](actions/schedule-windows.md) | `GET /company/schedule_availability` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/898190c92fb8b-schedule-windows) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customer_id` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/b1c3acd657849-update-customer) |
| [Update Job Schedule](actions/update-job-schedule.md) | `PUT /jobs/:job_id/schedule` | [docs](https://docs.housecallpro.com/docs/housecall-public-api/1d344f58672f9-update-job-schedule) |
