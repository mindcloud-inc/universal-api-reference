# Create Channel with Twist

Creates a new channel in Twist.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/add`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Create Channel](https://developer.twist.com/v3/#add-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | no | The description of the channel. |
| `name` | query | `string` | yes | The name of the new channel. |
| `public` | query | `boolean` | no | If enabled, the channel will be marked as public. |
| `workspace_id` | query | `number` | yes | The id of the workspace. |
