# [Beta] Change A Feature Environment Safeguard with Unleash

Changes a feature environment safeguard in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/safeguards`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Change A Feature Environment Safeguard](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
