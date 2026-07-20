# Create Agent with Ringg AI

Creates an agent in Ringg AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/agent`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Create Agent](https://docs.ringg.ai/api-reference/endpoint/assistant/create-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_name` | body | `string` | yes | (Required) Name of the agent Maximum length: 100. |
| `introduction_and_objective` | body | `string` | yes | (Required) Introduction and objective of the agent Maximum length: 2000. |
| `response_guidelines` | body | `string` | yes | (Required) Guidelines for how the agent should respond Maximum length: 3000. |
| `task` | body | `string` | yes | (Required) The task the agent should perform Maximum length: 1500. |
| `faq` | body | `string` | no | (Optional) FAQ content for the agent Maximum length: 5000. |
| `sample_conversations` | body | `string` | no | (Optional) Example conversations for the agent. Use \n for newlines between turns. Maximum length: 5000. |
| `primary_language` | body | `string` | yes | (Required) Primary language locale for the agent |
| `secondary_language` | body | `string` | no | (Optional) Secondary language locale for the agent |
| `voice_id` | body | `string` | yes | (Required) Internal AgentVoice ID (UUID). Get available voices from the Get Assistant Voices endpoint. |
| `intro_message` | body | `string` | yes | (Required) Introduction message the agent will speak when the call starts Maximum length: 500. |
| `agent_type` | body | `string` | no | (Required) Type of agent. Defaults to outbound. |
| `custom_variables[]` | body | `array<string>` | no | (Optional) Custom variables for the agent. For outbound agents, callee_name and mobile_number are always included automatically. |
