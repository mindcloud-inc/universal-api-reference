# [Beta] Get Strategies That Use A Context Field with Unleash

Retrieves strategies that use a context field from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/projects/{projectId}/context/{contextField}/strategies`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Get Strategies That Use A Context Field](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `contextField` | path | `string` | yes | Required path parameter. |
