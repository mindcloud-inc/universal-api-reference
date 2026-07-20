# Create Connection with Are.na

Creates a new connection in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `connections`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Create Connection](https://www.are.na/developers/explore/connection/post-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_ids[]` | body | `array<number>` | yes | Array of channel IDs to connect the item into. |
| `connectable_id` | body | `number` | yes | ID of the block or channel to connect. |
| `connectable_type` | body | `string` | yes | Type of item to connect: Block or Channel. |
