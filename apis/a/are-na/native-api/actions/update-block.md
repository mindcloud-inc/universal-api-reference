# Update Block with Are.na

Updates an existing block in Are.na.

## Endpoint

- **Method:** `PUT`
- **Path:** `blocks/:id`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Update Block](https://www.are.na/developers/explore/block/put-block)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Updated text content for text blocks. |
| `description` | body | `string` | no | Updated block description. |
| `id` | path | `string` | no | Are.na block ID. |
| `title` | body | `string` | no | Updated block title. |
