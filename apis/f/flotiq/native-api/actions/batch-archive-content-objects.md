# Batch Archive Content Objects with Flotiq

Archives multiple content objects in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/batch-archive`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Batch Archive Content Objects](https://flotiq.com/docs/API/draft-public/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that owns the objects. |
| `body` | body | `object` | yes | The batch archive payload. |
