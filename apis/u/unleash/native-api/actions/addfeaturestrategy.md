# Add A Strategy To A Feature Flag with Unleash

Adds a strategy to a feature flag in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Add A Strategy To A Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
