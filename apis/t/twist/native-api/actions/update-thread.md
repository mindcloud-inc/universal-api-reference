# Update Thread with Twist

Updates an existing thread in Twist.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/update`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Update Thread](https://developer.twist.com/v3/#update-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | query | `string` | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `content` | query | `string` | no | The content of the thread. |
| `id` | query | `number` | yes | The id of the thread. |
| `title` | query | `string` | no | The title of the thread. |
