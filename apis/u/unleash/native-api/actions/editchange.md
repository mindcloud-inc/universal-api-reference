# Edits A Single Change In A Change Request with Unleash

Edits a single change in a change request in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{projectId}/change-requests/{changeRequestId}/changes/{changeId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Edits A Single Change In A Change Request](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `changeRequestId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `changeId` | path | `string` | yes | Required path parameter. |
