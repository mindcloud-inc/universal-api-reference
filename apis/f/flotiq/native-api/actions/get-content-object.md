# Get Content Object with Flotiq

Retrieves a content object from Flotiq.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/{{name}}/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Get Content Object](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the object. |
| `id` | path | `string` | yes | The Flotiq object ID. |
