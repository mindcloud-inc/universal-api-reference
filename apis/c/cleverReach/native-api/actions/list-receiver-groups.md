# List Receiver Groups with CleverReach

Retrieves groups for a receiver in CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/receivers.json/:id/groups`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [List Receiver Groups](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/receivers-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID or email of the receiver. |
| `state` | query | `string` | no | state of the receiver within the group. Accepted values: `0`, `1`, `2`. |
