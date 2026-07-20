# List jobs with Jobsoid

Retrieves published jobs from Jobsoid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/jobs`
- **Base URL:** `https://demo.jobsoid.com`
- **Official documentation:** [List jobs](https://apidocs.jobsoid.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search published jobs by job title. |
| `loc` | query | `list` | no | Filter jobs by location ID. |
| `dept` | query | `list` | no | Filter jobs by department ID. |
| `div` | query | `list` | no | Filter jobs by division ID. |
| `fun` | query | `list` | no | Filter jobs by job function ID. |
