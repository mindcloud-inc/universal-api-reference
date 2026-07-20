# Send Notification to Group with Vybit

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/following/{{key}}/send-to-group`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Send Notification to Group](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | body | `string` | no | Custom image URL |
| `key` | path | `string` | no | The unique key of the subscription following record. |
| `linkUrl` | body | `string` | no | Custom link URL |
| `message` | body | `string` | no | Notification message |
