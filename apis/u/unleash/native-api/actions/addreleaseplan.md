# Add A Release Plan. with Unleash

Adds a release plan in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Add A Release Plan.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
