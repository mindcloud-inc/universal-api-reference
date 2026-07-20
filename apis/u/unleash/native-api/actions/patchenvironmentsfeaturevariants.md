# Patch A Feature's Variants In An Environment with Unleash

Patches feature variants in an environment in Unleash.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Patch A Feature's Variants In An Environment](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
