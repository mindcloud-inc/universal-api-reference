# Update Content Type with Flotiq

Updates an existing content type in Flotiq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/internal/contenttype/{{id}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Update Content Type](https://flotiq.com/docs/API/content-types/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Flotiq content type ID. |
| `body` | body | `object` | yes | The updated content type definition payload. |
