# Update Push with Pushbullet

Updates an existing push in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/pushes/:push_iden`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Update Push](https://docs.pushbullet.com/v8/#pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `push_iden` | path | `string` | yes | Push identifier to update. |
| `dismissed` | body | `boolean` | no | Set true to dismiss a push, false to undismiss. |
| `items[]` | body | `array<object>` | no | Array of update entries for mirrored notifications. |
