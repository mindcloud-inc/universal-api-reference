# [Beta] Set Feature Completed with Unleash

Sets feature completed in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/lifecycle/complete`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Set Feature Completed](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `featureName` | path | `string` | yes | Required path parameter. |
