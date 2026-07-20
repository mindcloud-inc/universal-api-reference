# Create Content Object with Flotiq

Creates a new content object in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Create Content Object](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that will store the object. |
| `body` | body | `object` | yes | The content object payload to create. |
