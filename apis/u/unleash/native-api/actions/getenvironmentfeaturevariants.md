# Get Variants For A Feature In An Environment with Unleash

Retrieves variants for a feature in an environment from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/variants`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Get Variants For A Feature In An Environment](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
