# [Beta] Change A Release Plan Safeguard with Unleash

Changes a release plan safeguard in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/safeguards`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Change A Release Plan Safeguard](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `planId` | path | `string` | yes | Required path parameter. |
