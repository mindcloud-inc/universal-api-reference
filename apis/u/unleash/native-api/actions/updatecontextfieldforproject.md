# [Beta] Update An Existing Context Field with Unleash

Updates an existing context field in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/projects/{projectId}/context/{contextField}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Update An Existing Context Field](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `contextField` | path | `string` | yes | Required path parameter. |
