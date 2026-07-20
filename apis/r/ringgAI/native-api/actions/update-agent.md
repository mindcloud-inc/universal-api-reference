# Update Agent with Ringg AI

Updates an existing agent in Ringg AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/public/agent/:agent_id`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | (Required) The unique ID of the agent to update |
| `agent_name` | body | `string` | no | (Optional) Name of the agent Maximum length: 100. |
| `introduction_and_objective` | body | `string` | no | (Optional) Introduction and objective of the agent Maximum length: 2000. |
| `response_guidelines` | body | `string` | no | (Optional) Guidelines for how the agent should respond Maximum length: 3000. |
| `task` | body | `string` | no | (Optional) The task the agent should perform Maximum length: 1500. |
| `faq` | body | `string` | no | (Optional) FAQ content for the agent Maximum length: 5000. |
| `sample_conversations` | body | `string` | no | (Optional) Example conversations for the agent. Use \n for newlines between turns. Maximum length: 5000. |
| `primary_language` | body | `string` | no | (Optional) Primary language locale for the agent |
| `secondary_language` | body | `string` | no | (Optional) Secondary language locale for the agent |
| `voice_id` | body | `string` | no | (Optional) Internal AgentVoice ID (UUID). Get available voices from the Get Assistant Voices endpoint. |
| `intro_message` | body | `string` | no | (Optional) Introduction message the agent will speak when the call starts Maximum length: 500. |
| `agent_type` | body | `string` | no | (Optional) Type of agent |
| `custom_variables[]` | body | `array<string>` | no | (Optional) Custom variables for the agent. For outbound agents, callee_name and mobile_number cannot be removed. |
