# List Time Limits with Insightful

Finds time limits in Insightful by project or employee.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-limit`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [List Time Limits](https://developers.insightful.io/#bdafd15c-8d56-4e87-9ca4-551d2df8b79f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | query | `string` | no | Filter by employee ID. |
| `projectId` | query | `string` | no | Filter by project ID. |
| `type` | query | `string` | no | Filter by duration type: day, week, or month. |
