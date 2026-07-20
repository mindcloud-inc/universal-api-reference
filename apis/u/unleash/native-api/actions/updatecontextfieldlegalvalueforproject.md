# [Beta] Add Or Update Legal Value For The Context Field with Unleash

Adds or update legal value for the context field in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/projects/{projectId}/context/{contextField}/legal-values`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Add Or Update Legal Value For The Context Field](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `contextField` | path | `string` | yes | Required path parameter. |
