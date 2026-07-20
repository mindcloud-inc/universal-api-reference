# Create Note with Chatvolt AI

Creates a note in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/notes`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Note](https://docs.chatvolt.ai/api-reference/endpoint/conversation/create-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation to add a note to. |
| `note` | body | `string` | yes | Text content of the note (max 500 characters). |
| `isPrivate` | body | `boolean` | no | Whether the note is private. |
| `isJustify` | body | `boolean` | no | Whether the note is a justification (admin only). |
| `notificationDateTime` | body | `string` | no | Date and time for a notification, if any. |
