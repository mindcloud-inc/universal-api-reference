# Patch Media Object with Flotiq

Updates part of a media object in Flotiq.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/content/_media/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Patch Media Object](https://flotiq.com/docs/API/media/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Flotiq media object ID. |
| `body` | body | `object` | yes | The partial media object payload. |
