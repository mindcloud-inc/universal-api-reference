# List Jobs with Leap

Retrieves job records from Leap.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [List Jobs](https://docs.api.jobprogress.com/api/job.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | no | Search jobs by keyword. |
| `limit` | query | `number` | no | Number of jobs to return, up to 100. |
| `page` | query | `number` | no | Page number for pagination. |
