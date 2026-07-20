# Add Order Item with Everbill

Creates a new order item in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/add_item/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Add Order Item](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1add_item~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `article_id` | body | `number` | no | article_id request body field. |
| `new` | body | `boolean` | no | new request body field. |
| `name` | body | `string` | no | name request body field. |
| `quantity` | body | `number` | no | quantity request body field. |
| `description` | body | `string` | no | description request body field. |
| `unit` | body | `string` | no | unit request body field. |
| `price` | body | `number` | no | price request body field. |
| `ust` | body | `number` | no | ust request body field. |
