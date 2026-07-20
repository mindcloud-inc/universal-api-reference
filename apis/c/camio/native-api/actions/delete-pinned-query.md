# Delete Pinned Query with Camio

Deletes a pinned query from Camio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:user/queries/pinned/:id`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Delete Pinned Query](https://api.camio.com/#deleta-a-pinned-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The pinned query id to delete. |
