# List Job Positions with SharpAPI

Retrieves job positions from SharpAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/utilities/job_positions_list`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [List Job Positions](https://sharpapi.com/en/catalog/utility/job-positions-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Optional job position name filter. |
| `include_related` | query | `boolean` | no | Whether to include related job positions. |
| `page` | query | `number` | no | Page number to retrieve. |
| `per_page` | query | `number` | no | Number of job positions to return per page. |
