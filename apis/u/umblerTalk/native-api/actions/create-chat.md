# Create Chat with Umbler Talk

Finds a chat in Umbler Talk, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Chat](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | body | `string` | yes | The channel ID for the chat. |
| `contactId` | body | `string` | yes | The contact ID to open a chat for. |
| `organizationId` | body | `string` | yes | The organization ID. |
