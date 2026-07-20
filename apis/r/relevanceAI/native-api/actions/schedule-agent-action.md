# Schedule Action In Task with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/scheduled_triggers_item/create`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Schedule Action In Task](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The Relevance AI agent id. |
| `conversation_id` | body | `string` | yes | The task conversation id to schedule against. |
| `message` | body | `string` | yes | The follow-up message to schedule. |
| `minutes_until_schedule` | body | `number` | no | How many minutes from now to schedule the action. |
