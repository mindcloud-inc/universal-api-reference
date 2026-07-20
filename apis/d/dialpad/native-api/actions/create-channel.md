# Create Channel with Dialpad

Creates a new channel in Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Create Channel](https://developers.dialpad.com/reference/channelspost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | [single-line only] The name of the channel. |
| `description` | body | `string` | yes | The description of the channel. |
| `privacy_type` | body | `list<string>` | yes | The privacy type of the channel. Accepted values: `private`, `public`. |
| `user_id` | body | `number` | no | The ID of the user who owns the channel. Just for company level API key. |
