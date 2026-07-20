# List Boards with Miro

Retrieves boards from Miro.

## Endpoint

- **Method:** `GET`
- **Path:** `/boards`
- **Base URL:** `https://api.miro.com/v2`
- **Official documentation:** [List Boards](https://developers.miro.com/reference/get-boards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of boards to return. |
| `cursor` | query | `string` | no | Pagination cursor returned by the previous request. |
