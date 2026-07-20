# Create Time Limit with Insightful

Creates a new time limit in Insightful.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-limit`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Create Time Limit](https://developers.insightful.io/#a3fd95eb-18b7-40c2-a611-48d5f07c12cc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | body | `string` | no | Optional employee ID. Use * for a default project limit. |
| `limit` | body | `number` | yes | The limit in minutes. |
| `projectId` | body | `string` | yes | The project ID for the limit. |
| `start` | body | `string` | yes | The start date and time in YYYY-MM-DD HH:MM:SS format. |
| `timezone` | body | `string` | no | Optional IANA timezone. |
| `type` | body | `string` | yes | The duration type: day, week, or month. |
