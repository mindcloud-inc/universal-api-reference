# Push Stream Data with Instasent

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project/datasource/:datasource/stream/:action`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Push Stream Data](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | path | `string` | yes | Datasource identifier. |
| `action` | path | `string` | yes | Stream action name. |
| `_sync` | query | `boolean` | no | Whether to process the stream request synchronously. |
| `records[]` | body | `array<object>` | yes | Stream records to push. |
