# Reject Time Request with WebWork Time Tracker

Rejects a time request in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-requests/:timeRequestId/reject`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Reject Time Request](https://api-docs.webwork-tracker.com/api/time-requests/rejecttimerequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeRequestId` | path | `string` | yes | Encrypted time request ID. |
| `workspace_id` | body | `number` | yes | Workspace ID. |
| `comment` | body | `string` | yes | Comment explaining the rejection reason. |
