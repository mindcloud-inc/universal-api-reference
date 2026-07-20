# Trigger Vybit Notification with Vybit

## Endpoint

- **Method:** `POST`
- **Path:** `/vybit/{{key}}/trigger`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Trigger Vybit Notification](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | body | `string` | no | Custom image URL |
| `key` | path | `string` | yes | The unique key of the vybit to trigger. |
| `linkUrl` | body | `string` | no | Custom link URL |
| `log` | body | `string` | no | Log entry to append to the vybit log |
| `message` | body | `string` | no | Custom notification message |
| `runOnce` | body | `boolean` | no | Disable the vybit after this trigger fires |
