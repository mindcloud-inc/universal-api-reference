# Update Subscription Following with Vybit

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscription/following/{{key}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Update Subscription Following](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessStatus` | body | `string` | no | Accept or decline a subscription invitation |
| `imageUrl` | body | `string` | no | Custom image URL for notifications |
| `key` | path | `string` | yes | The unique key of the subscription following record. |
| `linkUrl` | body | `string` | no | Custom link URL for notifications |
| `message` | body | `string` | no | Custom notification message |
| `status` | body | `string` | no | Enable or disable notifications for this subscription |
