# Edit Message Draft with Front

Updates an existing message draft in Front.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/drafts/:message_id/`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Edit Message Draft](https://dev.frontapp.com/reference/edit-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | The draft ID. |
| `body` | body | `string` | yes | Body of the draft. |
| `channel_id` | body | `string` | yes | ID of the channel from which the draft will be sent. |
| `version` | body | `string` | no | Version of the draft. |
