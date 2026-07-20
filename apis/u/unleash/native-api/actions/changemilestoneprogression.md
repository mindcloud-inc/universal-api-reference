# [Beta] Create Or Update A Milestone Progression with Unleash

Creates new or update a milestone progression in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{id}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Create Or Update A Milestone Progression](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `id` | path | `string` | yes | Required path parameter. |
