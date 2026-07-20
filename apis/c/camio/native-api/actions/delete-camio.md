# Delete Camio with Camio

Deletes a Camio from Camio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/me/camios`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Delete Camio](https://api.camio.com/#delete-camio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Observed runtime requires the Camio id alongside the view token for reliable deletion. |
| `view_token` | query | `string` | yes | The Camio view token to delete. |
