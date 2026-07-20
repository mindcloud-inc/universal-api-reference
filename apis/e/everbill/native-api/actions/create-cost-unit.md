# Create Cost Unit with Everbill

Creates a new cost unit in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/cost_units/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Cost Unit](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1cost_units~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | name request body field. |
| `number` | body | `string` | no | number request body field. |
