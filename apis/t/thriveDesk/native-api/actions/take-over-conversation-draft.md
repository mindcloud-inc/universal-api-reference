# Take Over Conversation Draft with ThriveDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversation/{{conversationId}}/draft/{{eventId}}/take-over`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Take Over Conversation Draft](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | no | The conversation ID. |
| `eventId` | path | `string` | yes | The draft event ID. |
