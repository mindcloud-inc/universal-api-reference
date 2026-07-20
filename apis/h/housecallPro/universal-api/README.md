# <img src="https://images.mindcloud.co/apps/icons/images_1773185171372.png" alt="Housecall Pro logo" width="28" height="28"> Housecall Pro: Universal API

Manage customers, jobs, estimates, employees, and schedules

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/housecallPro/latest
- **Category:** Support / Field Service
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.housecallpro.com/
- **Vendor API docs:** https://docs.housecallpro.com/docs/housecall-public-api/a4ca20a18010c-housecall-v1-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET |  |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Estimate Option Line Items](actions/bulk-update-estimate-option-line-items.md) | PUT |  |
| [Create Estimate](actions/create-estimate.md) | POST |  |
| [Get Estimate](actions/get-estimate.md) | GET |  |
| [List Estimates](actions/list-estimates.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [List Job Invoices](actions/list-job-invoices.md) | GET |  |
| [Preview Invoice by UUID](actions/preview-invoice-by-uuid.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Update Job Schedule](actions/update-job-schedule.md) | PUT |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Convert Lead to Estimate or Job](actions/convert-lead-to-estimate-or-job.md) | POST |  |
| [Create Lead](actions/create-lead.md) | POST |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |

### Schedule Window

| Action | Method | Description |
| --- | --- | --- |
| [Schedule Windows](actions/schedule-windows.md) | GET |  |

