# Create Project with Everbill

Creates a new project in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Project](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1projects~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | name request body field. |
| `archiv` | body | `boolean` | no | archiv request body field. |
| `notices` | body | `string` | no | notices request body field. |
