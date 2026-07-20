# Create Orchestration with eGain

Creates a new orchestration in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/orchestrations`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Orchestration](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/orchestration/createorchestration.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the orchestration is active. |
| `applications.botConfiguration.bots[0].id` | body | `string` | yes | Bot client application ID. |
| `applications.botConfiguration.bots[0].onEscalation.agent.id` | body | `string` | yes | Agent application ID used on escalation. |
| `applications.botConfiguration.bots[0].participant.id` | body | `string` | yes | Bot participant ID. |
| `applications.customerConfiguration.customer.id` | body | `string` | yes | Customer application ID. |
| `description` | body | `string` | no | Orchestration description. |
| `name` | body | `string` | yes | Orchestration name. |
