# [Beta] Delete A Milestone Progression with Unleash

Deletes a milestone progression from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{id}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Delete A Milestone Progression](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `id` | path | `string` | yes | Required path parameter. |
