# Get Feature Flag Strategies with Unleash

Retrieves feature flag strategies from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Get Feature Flag Strategies](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
