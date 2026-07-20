# Emit Session Event with Voiceflow

Sends an event to an active Voiceflow session.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/project/:projectId/session/:sessionId/event`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Emit Session Event](https://docs.voiceflow.com/api-reference/session/emit-session-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Unique ID of the conversation session. |
| `action` | body | `object` | yes | The event to send to the active conversation. |
