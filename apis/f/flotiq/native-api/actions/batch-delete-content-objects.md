# Batch Delete Content Objects with Flotiq

Deletes multiple content objects from Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/batch-delete`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Batch Delete Content Objects](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the objects. |
| `body` | body | `object` | yes | The batch delete payload. |
