# Get Media Image with Flotiq

Retrieves a transformed media image from Flotiq.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.flotiq.com/image/{{widthHeight}}/{{key}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Get Media Image](https://flotiq.com/docs/API/media/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widthHeight` | path | `string` | yes | The image size preset, for example 400x400. |
| `key` | path | `string` | yes | The media object key or filename reference. |
