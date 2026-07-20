# Scroll Audience with Instasent

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project/audience/scroll`
- **Base URL:** `https://api.instasent.com/v1`
- **Official documentation:** [Scroll Audience](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `root` | body | `object` | no | Audience filter tree to scroll. |
| `limit` | body | `number` | no | Maximum number of results to return per page. |
| `cursor` | body | `string` | no | Pagination cursor from the previous scroll response. |
