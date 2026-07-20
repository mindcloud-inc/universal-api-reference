# Get User Message Limit with Agenthost.ai

Retrieves a user's message limit from Agenthost.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/openai/user_message_limit/`
- **Base URL:** `https://api.agenthost.ai`
- **Official documentation:** [Get User Message Limit](https://docs.agenthost.ai/custom-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Optional email address to check a specific user's message limit. |
