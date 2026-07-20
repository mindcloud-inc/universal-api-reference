# Get Event Parameter Specs with Instasent

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project/specs/events/:eventType`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Get Event Parameter Specs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `eventType` | path | `string` | yes | Event type slug to inspect. |
