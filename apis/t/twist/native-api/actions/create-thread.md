# Create Thread with Twist

Creates a new thread in a Twist channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/add`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Create Thread](https://developer.twist.com/v3/#add-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | query | `string` | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `channel_id` | query | `number` | yes | The id of the channel. |
| `content` | query | `string` | yes | The content of the new thread. |
| `recipients` | query | `string` | no | Users that will be attached to the thread. |
| `send_as_integration` | query | `boolean` | no | Displays the integration as the thread creator. |
| `title` | query | `string` | yes | The title of the new thread. |
