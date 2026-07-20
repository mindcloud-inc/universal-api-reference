# Convert Definition by URL with Swagger Converter

Retrieves a converted OpenAPI document from Swagger Converter by source URL.

## Endpoint

- **Method:** `GET`
- **Path:** `convert`
- **Base URL:** `https://converter.swagger.io/api/`
- **Official documentation:** [Convert Definition by URL](https://converter.swagger.io/api/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | A URL to the Swagger/OpenAPI 1.x or 2.x definition to convert. |
