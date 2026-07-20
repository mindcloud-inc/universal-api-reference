# Convert Definition by Content with Swagger Converter

Creates a converted OpenAPI document in Swagger Converter from input content.

## Endpoint

- **Method:** `POST`
- **Path:** `convert`
- **Base URL:** `https://converter.swagger.io/api/`
- **Official documentation:** [Convert Definition by Content](https://converter.swagger.io/api/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `specification` | body | `object` | yes | The Swagger/OpenAPI 1.x or 2.x specification object to convert. |
