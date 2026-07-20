# Create/Add Change To A Change Request with Unleash

Creates or adds a change to a request in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/environments/{environment}/change-requests`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Create/Add Change To A Change Request](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
