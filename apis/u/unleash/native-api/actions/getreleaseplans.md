# Get Release Plans. with Unleash

Retrieves release plans from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Get Release Plans.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureName` | path | `string` | yes | Required path parameter. |
| `project` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
