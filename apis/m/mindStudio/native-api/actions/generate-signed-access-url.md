# Generate Signed Access URL with MindStudio

Creates a signed access URL for a MindStudio agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate-signed-access-url`
- **Base URL:** `https://api.mindstudio.ai/developer/v2`
- **Official documentation:** [Generate Signed Access URL](https://university.mindstudio.ai/docs/deployment-of-ai-agents/embedding-ai-agents#getting-the-signed-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The MindStudio agent ID to generate a signed access URL for. |
| `userId` | body | `string` | no | Optional unique user identifier for the signed access session. |
