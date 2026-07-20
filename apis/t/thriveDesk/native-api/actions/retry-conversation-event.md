# Retry Conversation Event with ThriveDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations/{{conversationId}}/events/{{eventId}}/retry`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Retry Conversation Event](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The conversation ID. |
| `eventId` | path | `string` | yes | The event ID. |
