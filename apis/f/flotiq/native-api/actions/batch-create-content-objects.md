# Batch Create Content Objects with Flotiq

Creates multiple content objects in Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/{{name}}/batch`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Batch Create Content Objects](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name that will store the objects. |
| `body` | body | `object` | yes | The batch payload to create objects. |
