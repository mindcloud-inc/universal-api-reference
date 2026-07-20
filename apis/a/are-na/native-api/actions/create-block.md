# Create Block with Are.na

Creates a new block in Are.na.

## Endpoint

- **Method:** `POST`
- **Path:** `blocks`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [Create Block](https://www.are.na/developers/explore/block/post-block)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_ids[]` | body | `array<number>` | yes | Array of channel IDs where the block should be added. |
| `content` | body | `string` | no | Text content or URL for the block. |
| `title` | body | `string` | no | Optional block title. |
| `value` | body | `string` | no | Text, markdown, URL, or other value to create the block from. |
