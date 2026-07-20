# Send Reaction with Stream

Creates a reaction for a Stream message.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:id/reaction`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Send Reaction](https://getstream.io/chat/docs/javascript/send_reaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message ID. |
| `reaction` | body | `object` | yes | Reaction payload. |
