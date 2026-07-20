# Update Live Job Debug Params with Gladia

Updates live job debug parameters in Gladia.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/live/:id`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Update Live Job Debug Params](https://api.gladia.io/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gladia live job identifier. |
| `post_session_metadata` | body | `object` | no | Debug metadata object stored in the live job request params after the session ends. |
