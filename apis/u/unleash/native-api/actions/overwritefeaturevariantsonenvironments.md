# Create (Overwrite) Variants For A Feature Flag In Multiple Environments with Unleash

Creates or overwrites feature variants across environments in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/variants-batch`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Create (Overwrite) Variants For A Feature Flag In Multiple Environments](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `featureName` | path | `string` | yes | Required path parameter. |
