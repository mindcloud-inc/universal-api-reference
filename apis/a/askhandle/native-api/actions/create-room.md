# Create Room with AskHandle

Creates a new room in AskHandle.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Create Room](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Room name. |
| `is_bot_use` | body | `boolean` | no | Whether the bot is enabled. |
