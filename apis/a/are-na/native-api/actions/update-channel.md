# Update Channel with Are.na

Updates an existing channel in Are.na.

## Endpoint

- **Method:** `PUT`
- **Path:** `channels/:id`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Update Channel](https://www.are.na/developers/explore/channel/put-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated markdown description. |
| `id` | path | `string` | no | Are.na channel ID or slug. |
| `title` | body | `string` | no | Updated channel title. |
| `visibility` | body | `string` | no | Updated visibility: public, closed, or private. |
