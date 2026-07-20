# Reply to Message with ChipBot

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/connect/accounts/:accountId/domains/:domainId/messages`
- **Base URL:** `https://getchipbot.com`
- **Official documentation:** [Reply to Message](https://getchipbot.com/api-docs/chat-api/reply-to-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email from the incoming chat message webhook payload. |
| `message` | body | `string` | yes | Reply content to send back to the thread. |
