# Create Comment with Twist

Creates a new comment in a Twist thread.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/add`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Create Comment](https://developer.twist.com/v3/#add-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | query | `string` | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `content` | query | `string` | yes | The content of the new comment. |
| `recipients` | query | `string` | no | Users to notify. |
| `send_as_integration` | query | `boolean` | no | Displays the integration as the comment creator. |
| `thread_action` | query | `string` | no | Can be close or reopen. |
| `thread_id` | query | `number` | yes | The id of the thread. |
