# Delete A Strategy From A Feature Flag with Unleash

Deletes a strategy from a feature flag from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/{strategyId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Delete A Strategy From A Feature Flag](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `strategyId` | path | `string` | yes | Required path parameter. |
