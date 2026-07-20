# Get Monari Agent Response with Mona AI

Gets a response from a Mona AI Monari agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/getMonariAgentResponse`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Monari Agent Response](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | Monari agent identifier to execute. |
| `language_code` | body | `string` | no | Language code for the response; docs default to DE. |
| `permission` | body | `string` | yes | Mona permission string required by the Monari agent response endpoint. |
| `prompt` | body | `string` | yes | Prompt to send to the Monari agent. |
| `sessionId` | body | `string` | no | Monari agent session identifier. |
