# Set Strategy Sort Order with Unleash

Sets strategy sort order in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/features/{featureName}/environments/{environment}/strategies/set-sort-order`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Set Strategy Sort Order](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `featureName` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `environment` | path | `string` | yes | Required path parameter. |
