# [Beta] Resume Paused Milestone Progressions with Unleash

Resumes paused milestone progressions in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{planId}/resume`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Resume Paused Milestone Progressions](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
| `planId` | path | `string` | yes | Required path parameter. |
