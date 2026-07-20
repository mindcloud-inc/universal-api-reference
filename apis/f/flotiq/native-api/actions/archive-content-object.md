# Archive Content Object with Flotiq

Archives a content object in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/{{id}}/archive`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Archive Content Object](https://flotiq.com/docs/API/draft-public/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the object. |
| `id` | path | `string` | yes | The Flotiq object ID. |
