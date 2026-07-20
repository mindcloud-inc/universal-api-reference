# Updates Change Request Configuration For An Environment In The Project with Unleash

Updates change request configuration for an environment in the project in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{projectId}/environments/{environment}/change-requests/config`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Updates Change Request Configuration For An Environment In The Project](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
