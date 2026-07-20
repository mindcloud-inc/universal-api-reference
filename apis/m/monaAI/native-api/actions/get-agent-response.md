# Get Agent Response with Mona AI

Gets a response from a Mona AI agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/getAgentResponse`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Agent Response](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `additional_info` | body | `string` | no | Optional additional context for the agent request. |
| `agentId` | body | `string` | yes | Mona agent identifier to execute. |
| `document_link` | body | `string` | no | Optional document link to include with the agent request. |
| `document_name` | body | `string` | no | Optional document name to include with the agent request. |
| `language_code` | body | `string` | no | Language code for the agent response; docs default to DE. |
| `permission` | body | `string` | yes | Mona permission string for agent execution; docs show executeAgents for this endpoint. |
| `prompt` | body | `string` | yes | Prompt to send to the agent. |
| `session_id` | body | `string` | no | Agent session identifier. |
