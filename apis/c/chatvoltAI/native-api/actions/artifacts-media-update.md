# Update Media with Chatvolt AI

Updates a media in Chatvolt AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/artifacts/media/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Media](https://docs.chatvolt.ai/api-reference/endpoint/artifacts/media/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | Name for application/json requests. |
| `altDescription` | body | `string` | no | AltDescription for application/json requests. |
| `isActive` | body | `boolean` | no | IsActive for application/json requests. |
