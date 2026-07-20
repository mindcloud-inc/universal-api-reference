# Get Job Results with NeverBounce

Retrieves detailed job results from NeverBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/results`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Get Job Results](https://developers.neverbounce.com/reference/jobs-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `number` | yes | NeverBounce job identifier. |
| `page` | query | `number` | no | Results page to retrieve. |
| `items_per_page` | query | `number` | no | Number of results to return per page. |
