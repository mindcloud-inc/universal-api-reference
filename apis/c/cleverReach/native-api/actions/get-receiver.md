# Get Receiver with CleverReach

Retrieves a receiver from CleverReach by receiver ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/receivers.json/:id`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [Get Receiver](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/receivers-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID or email of the receiver. |
| `group_id` | query | `string` | no | ID of group for group specific information. |
