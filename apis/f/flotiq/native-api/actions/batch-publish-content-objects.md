# Batch Publish Content Objects with Flotiq

Publishes multiple content objects in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/batch-publish`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Batch Publish Content Objects](https://flotiq.com/docs/API/draft-public/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the objects. |
| `body` | body | `object` | yes | The batch publish payload. |
