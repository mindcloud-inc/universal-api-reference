# Update Room with AskHandle

Updates an existing AskHandle room by label.

## Endpoint

- **Method:** `PUT`
- **Path:** `/rooms/:label/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Update Room](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#room)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | path | `string` | no | The room label. |
| `name` | body | `string` | no | Room name. |
| `rating` | body | `number` | no | Room rating. |
| `is_bot_use` | body | `boolean` | no | Whether the bot is enabled. |
