# This Endpoint Will Add A Comment To A Change Request with Unleash

Adds a comment to a change request in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/change-requests/{id}/comments`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [This Endpoint Will Add A Comment To A Change Request](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `id` | path | `string` | yes | Required path parameter. |
