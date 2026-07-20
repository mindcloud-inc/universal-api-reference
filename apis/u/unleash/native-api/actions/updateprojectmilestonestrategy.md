# [Beta] Update A Milestone Strategy with Unleash

Updates a milestone strategy in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/milestone-strategies/{strategyId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Update A Milestone Strategy](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `strategyId` | path | `string` | yes | Required path parameter. |
