# Update Orchestration with eGain

Updates an existing orchestration in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orchestrations/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Orchestration](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/updateorchestration.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether orchestration is active. |
| `applications.botConfiguration.bots[0].id` | body | `string` | yes | Bot app ID. |
| `applications.botConfiguration.bots[0].onEscalation.agent.id` | body | `string` | yes | Escalation agent app ID. |
| `applications.botConfiguration.bots[0].participant.id` | body | `string` | yes | Bot participant ID. |
| `applications.customerConfiguration.customer.id` | body | `string` | yes | Customer app ID. |
| `description` | body | `string` | no | Orchestration description. |
| `id` | path | `string` | yes | Orchestration ID. |
| `name` | body | `string` | yes | Orchestration name. |
