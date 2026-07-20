# Reply To Message with Woodpecker.co

Replies to a message in the Woodpecker inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/inbox/messages/[:id]/reply`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Reply To Message](https://developers.woodpecker.co/docs/inbox/post-reply-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Inbox message ID from Woodpecker. |
