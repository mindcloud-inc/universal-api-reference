# Update Media Object with Flotiq

Updates an existing media object in Flotiq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/content/_media/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Update Media Object](https://flotiq.com/docs/API/media/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Flotiq media object ID. |
| `body` | body | `object` | yes | The replacement media object payload. |
