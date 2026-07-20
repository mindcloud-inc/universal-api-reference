# List Leaves with WebWork Time Tracker

Retrieves leaves from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/leaves`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Leaves](https://api-docs.webwork-tracker.com/api/leaves/getleaves)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
| `user_id` | query | `number` | no | Optional filter by user ID. |
| `policy_id` | query | `number` | no | Optional filter by leave policy ID. |
| `is_paid` | query | `string` | no | Optional filter by paid leave status using yes or no. |
| `date_from` | query | `string` | no | Optional start date filter in YYYY-MM-DD format. |
| `date_to` | query | `string` | no | Optional end date filter in YYYY-MM-DD format. |
| `status` | query | `string` | no | Optional filter by leave request status. |
