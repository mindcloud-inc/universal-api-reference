# Add Bill Transaction with Everbill

Creates a new bill transaction in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/bills/add_transaction/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Add Bill Transaction](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1add_transaction~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `sum` | body | `number` | no | sum request body field. |
| `date` | body | `string` | no | date request body field. |
| `type` | body | `string` | yes | type request body field. |
| `notes` | body | `string` | no | notes request body field. |
| `show` | body | `boolean` | no | show request body field. |
