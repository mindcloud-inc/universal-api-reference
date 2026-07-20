# Bulk Disable A List Of Features with Unleash

Disables a list of features in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/bulk_features/environments/{environment}/off`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Bulk Disable A List Of Features](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
