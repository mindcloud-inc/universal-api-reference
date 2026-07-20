# Enable A Feature Flag with Unleash

Enables a feature flag in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/on`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Enable A Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
