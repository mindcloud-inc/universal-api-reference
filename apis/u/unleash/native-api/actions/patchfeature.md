# Modify A Feature Flag with Unleash

Updates a feature flag in Unleash.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Modify A Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `featureName` | path | `string` | yes | Required path parameter. |
