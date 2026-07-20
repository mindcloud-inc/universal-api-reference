# Move Thread to Channel with Twist

Moves a thread to another Twist channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/move_to_channel`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Move Thread to Channel](https://developer.twist.com/v3/#move-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | The id of the thread. |
| `to_channel` | query | `number` | yes | The target channel's id. |
