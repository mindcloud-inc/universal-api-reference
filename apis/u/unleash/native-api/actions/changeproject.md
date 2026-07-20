# Move Feature To Project with Unleash

Moves a feature to a project in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/changeProject`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Move Feature To Project](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `featureName` | path | `string` | yes | Required path parameter. |
