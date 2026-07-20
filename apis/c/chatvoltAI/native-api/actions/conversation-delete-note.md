# Delete Note with Chatvolt AI

Deletes a note from Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/conversations/{conversationId}/notes/{noteId}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Delete Note](https://docs.chatvolt.ai/api-reference/endpoint/conversation/delete-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation. |
| `noteId` | path | `string` | yes | ID of the note to delete. |
