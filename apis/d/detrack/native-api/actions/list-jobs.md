# List Jobs with Detrack

Retrieves jobs from Detrack with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/dn/jobs`
- **Base URL:** `https://app.detrack.com/api/v2`
- **Official documentation:** [List Jobs](https://detrackapiv2.docs.apiary.io/#reference/jobs/list-create/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | Page number. |
| `limit` | query | `string` | no | Number of records per page. Maximum 100. |
| `sort` | query | `string` | no | Sort field; prefix with - for descending. |
| `type` | query | `string` | no | Filter jobs by type: Delivery or Collection. |
| `date` | query | `string` | no | Filter jobs by date in YYYY-MM-DD format. |
| `assign_to` | query | `string` | no | Filter jobs by assigned driver or vehicle. |
| `status` | query | `string` | no | Filter jobs by status; use commas for multiple values. |
| `do_number` | query | `string` | no | Filter jobs by D.O. number. |
| `query` | query | `string` | no | Free-text job search query. |
