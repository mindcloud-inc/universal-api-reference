# Start A Release Plan Milestone. with Unleash

Starts a release plan milestone in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/release-plans/{planId}/milestones/{milestoneId}/start`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Start A Release Plan Milestone.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `planId` | path | `string` | yes | Required path parameter. |
| `milestoneId` | path | `string` | yes | Required path parameter. |
