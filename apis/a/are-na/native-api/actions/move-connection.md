# Move Connection with Are.na

Moves a connection within a channel in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `connections/:id/move`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Move Connection](https://www.are.na/developers/explore/connection/post-move)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na connection ID. |
| `movement` | body | `string` | no | Movement strategy, e.g. insert_at. |
| `position` | body | `number` | no | Target position, 1-indexed. |
