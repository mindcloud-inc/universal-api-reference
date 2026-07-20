# List Time Requests with WebWork Time Tracker

Retrieves time requests from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-requests`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Time Requests](https://api-docs.webwork-tracker.com/api/time-requests/gettimerequests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | Workspace ID. |
| `date_from` | query | `string` | yes | Start date for filtering time requests. |
| `date_to` | query | `string` | yes | End date for filtering time requests. |
| `status` | query | `string` | no | Optional status filter. |
