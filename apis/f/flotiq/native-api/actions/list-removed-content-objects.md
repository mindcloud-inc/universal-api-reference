# List Removed Content Objects with Flotiq

Retrieves removed content objects from Flotiq.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/{{name}}/removed`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [List Removed Content Objects](https://flotiq.com/docs/API/content-objects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name to inspect for removed objects. |
