# Get Prompt Trace for Message with AssignX

Retrieves a prompt trace for an AssignX message.

## Endpoint

- **Method:** `GET`
- **Path:** `messages/:id/trace`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Get Prompt Trace for Message](https://docs.agentx.so/reference/get_api-v1-access-messages-id-trace-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message identifier from a conversation response. |
