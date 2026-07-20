# Search Audience with Instasent

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project/audience/search`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Search Audience](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `root` | body | `object` | no | Audience search filter tree. |
| `limit` | body | `number` | no | Maximum number of results to return. |
| `offset` | body | `number` | no | Number of results to skip. |
