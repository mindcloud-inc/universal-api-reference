# Add A Feature Dependency. with Unleash

Adds a feature dependency in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{child}/dependencies`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Add A Feature Dependency.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `child` | path | `string` | yes | Required path parameter. |
