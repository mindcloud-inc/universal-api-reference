# Update Smart View with Close

Updates an existing smart view in Close.

## Endpoint

- **Method:** `PUT`
- **Path:** `/saved_search/:id/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Update Smart View](https://developer.close.com/resources/smart-views/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique Smart View ID. |
| `name` | body | `string` | no | Smart view name. |
| `query` | body | `string` | no | Smart view query payload. |
| `type` | body | `string` | no | Smart view type. |
