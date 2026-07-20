# Delete Stream Record with Instasent

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:project/datasource/:datasource/stream/:action/:userId`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Delete Stream Record](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | path | `string` | yes | Datasource identifier. |
| `action` | path | `string` | yes | Stream action name. |
| `userId` | path | `string` | yes | Audience user identifier. |
