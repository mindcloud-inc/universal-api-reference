# Create Draft Reply with Front

Creates a draft reply in Front.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/drafts`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Create Draft Reply](https://dev.frontapp.com/reference/create-draft-reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
| `body` | body | `string` | yes | Body of the draft. |
| `channel_id` | body | `string` | yes | ID of the channel from which the draft will be sent. |
| `subject` | body | `string` | no | Subject of the draft. |
