# Search Jobs with NeverBounce

Finds NeverBounce jobs by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/search`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Search Jobs](https://developers.neverbounce.com/reference/jobs-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `number` | yes | NeverBounce job identifier. |
| `page` | query | `number` | no | Result page to retrieve. |
| `items_per_page` | query | `number` | no | Number of jobs to return per page. |
| `filename` | query | `string` | no | Filter jobs by filename. |
| `job_status` | query | `string` | no | Filter jobs by NeverBounce job status. |
