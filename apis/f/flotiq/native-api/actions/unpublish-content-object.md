# Unpublish Content Object with Flotiq

Unpublishes a content object in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/{{id}}/unpublish`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Unpublish Content Object](https://flotiq.com/docs/API/draft-public/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the object. |
| `id` | path | `string` | yes | The Flotiq object ID. |
