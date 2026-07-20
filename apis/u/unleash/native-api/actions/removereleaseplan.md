# Remove A Release Plan. with Unleash

Removes a release plan from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Remove A Release Plan.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `planId` | path | `string` | yes | Required path parameter. |
