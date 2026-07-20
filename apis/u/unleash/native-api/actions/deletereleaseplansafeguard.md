# [Beta] Delete A Release Plan Safeguard with Unleash

Deletes a release plan safeguard from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/safeguards/{safeguardId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Delete A Release Plan Safeguard](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `planId` | path | `string` | yes | Required path parameter. |
| `safeguardId` | path | `string` | yes | Required path parameter. |
