# Change Specific Properties Of A Strategy with Unleash

Changes specific strategy properties in Unleash.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Change Specific Properties Of A Strategy](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `strategyId` | path | `string` | yes | Required path parameter. |
