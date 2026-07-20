# Create (Overwrite) Variants For A Feature In An Environment with Unleash

Creates or overwrites feature variants in an environment in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Create (Overwrite) Variants For A Feature In An Environment](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
