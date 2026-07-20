# Update Content Object with Flotiq

Updates an existing content object in Flotiq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/content/{{name}}/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Update Content Object](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the object. |
| `id` | path | `string` | yes | The Flotiq object ID. |
| `body` | body | `object` | yes | The replacement content object payload. |
