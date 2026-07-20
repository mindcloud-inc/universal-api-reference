# List Company Find Jobs with profileAPI

Retrieves company search jobs from profileAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/find/jobs`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [List Company Find Jobs](https://documentation.profileapi.com/api-reference/list-company-find-jobs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional job status filter. Current docs state list jobs supports filtering by status. |
