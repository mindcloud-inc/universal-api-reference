# Get Tracked Hours Report with WebWork Time Tracker

Retrieves tracked hours reports from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/tracked-hours`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Get Tracked Hours Report](https://api-docs.webwork-tracker.com/api/reports/gettrackedhoursreport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
| `user_id` | query | `number` | no | Optional filter by specific user ID. |
| `start_date` | query | `string` | no | Optional start date for the report in YYYY-MM-DD format. |
| `end_date` | query | `string` | no | Optional end date for the report in YYYY-MM-DD format. |
