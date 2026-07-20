# Approve Time Request with WebWork Time Tracker

Approves a time request in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-requests/:timeRequestId/approve`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Approve Time Request](https://api-docs.webwork-tracker.com/api/time-requests/approvetimerequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeRequestId` | path | `string` | yes | Encrypted time request ID. |
| `workspace_id` | body | `number` | yes | Workspace ID. |
