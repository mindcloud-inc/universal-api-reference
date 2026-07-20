# Update Channel with Twist

Updates an existing channel in Twist.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/update`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Update Channel](https://developer.twist.com/v3/#update-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | The description of the channel. |
| `id` | query | `number` | yes | The id of the channel. |
| `name` | query | `string` | yes | The name of the channel. |
| `public` | query | `boolean` | no | If enabled, the channel will be marked as public. |
