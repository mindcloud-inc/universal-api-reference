# Batch Patch Content Objects with Flotiq

Updates multiple content objects in Flotiq.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/content/{{name}}/batch`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Batch Patch Content Objects](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the objects. |
| `body` | body | `object` | yes | The batch patch payload. |
