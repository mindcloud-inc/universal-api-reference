# Update Default Environment Variables with Convex

Updates default environment variables in Convex.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/update_default_environment_variables`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Update Default Environment Variables](https://docs.convex.dev/production/environment-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The Convex project ID. |
| `changes[]` | body | `array<object>` | yes | The environment variable changes to apply. |
