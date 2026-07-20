# Vote On Message with AgentX

Updates a message vote in AgentX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vote/message/:id`
- **Base URL:** `https://api.agentx.so/api/v1/access`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message Id |
| `conversationId` | body | `string` | no | Unique identifier for the conversation |
| `messageId` | body | `string` | no | Unique identifier for the message within the conversation |
| `agentId` | body | `string` | no | Unique identifier for the agent handling the conversation |
| `traceId` | body | `string` | no | Trace identifier for tracking the conversation flow |
| `vote` | body | `number` | no | Vote value, for example 1 positive, 0 neutral, -1 negative |
