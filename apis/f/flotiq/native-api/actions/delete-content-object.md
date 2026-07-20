# Delete Content Object with Flotiq

Deletes an existing content object from Flotiq.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/content/{{name}}/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Delete Content Object](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the object. |
| `id` | path | `string` | yes | The Flotiq object ID. |
