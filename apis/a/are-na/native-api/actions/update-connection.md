# Update Connection with Are.na

Updates an existing connection in Are.na.

## Endpoint

- **Method:** `PUT`
- **Path:** `connections/:id`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Update Connection](https://www.are.na/developers/explore/connection/put-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na connection ID. |
| `metadata` | body | `object` | no | Metadata object to merge into the connection. |
