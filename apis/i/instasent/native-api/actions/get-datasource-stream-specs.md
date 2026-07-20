# Get Datasource Stream Specs with Instasent

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project/datasource/:datasource/stream/specs/:spec`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Get Datasource Stream Specs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | path | `string` | yes | Datasource identifier. |
| `spec` | path | `string` | yes | Specification identifier. |
