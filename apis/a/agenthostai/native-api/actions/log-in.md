# Log In with Agenthost.ai

Starts or completes Agenthost.ai login by email verification.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/openai/log_in/`
- **Base URL:** `https://api.agenthost.ai`
- **Official documentation:** [Log In](https://docs.agenthost.ai/custom-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user's email address. |
| `code` | body | `string` | no | Code sent to the user's email. |
