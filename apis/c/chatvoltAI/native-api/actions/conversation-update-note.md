# Update Note with Chatvolt AI

Updates a note in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/{conversationId}/notes/{noteId}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Note](https://docs.chatvolt.ai/api-reference/endpoint/conversation/update-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation. |
| `noteId` | path | `string` | yes | ID of the note to update. |
| `note` | body | `string` | no | Updated text content of the note. |
| `isPrivate` | body | `boolean` | no | Updated privacy status. |
| `notificationDateTime` | body | `string` | no | Updated notification date and time. |
