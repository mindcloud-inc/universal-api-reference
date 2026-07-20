# Set Environment Default Strategy with Unleash

Sets environment-default strategy in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/environments/{environment}/default-strategy`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Set Environment Default Strategy](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
