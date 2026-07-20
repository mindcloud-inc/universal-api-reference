# List Timesheets with WebWork Time Tracker

Retrieves timesheets from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/timesheets`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Timesheets](https://api-docs.webwork-tracker.com/api/timesheets/gettimesheets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
| `status` | query | `string` | no | Optional filter by timesheet status. |
| `date_from` | query | `string` | no | Optional start date filter in YYYY-MM-DD format. |
| `date_to` | query | `string` | no | Optional end date filter in YYYY-MM-DD format. |
| `user_id` | query | `number` | no | Optional filter by user ID. |
| `order_by` | query | `string` | no | Optional sort order by created_at using asc or desc. |
