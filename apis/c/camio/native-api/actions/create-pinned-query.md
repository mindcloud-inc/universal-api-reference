# Create Pinned Query with Camio

Creates a pinned query in Camio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:user/queries/pinned`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Create Pinned Query](https://api.camio.com/#create-a-pinned-query)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | A unique id for the pinned query. |
| `text` | body | `string` | yes | The pinned Camio query text. |
