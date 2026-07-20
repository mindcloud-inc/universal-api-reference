# Execute AI Agent with Cloud CLI

Runs an AI agent in a Cloud CLI environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/execute`
- **Base URL:** `https://cloudcli.ai/api/v1`
- **Official documentation:** [Execute AI Agent](https://developer.cloudcli.ai/execute-ai-agent-3998774e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | body | `string` | yes | ID of the running environment. |
| `projectName` | body | `string` | yes | Project folder name inside /workspace. |
| `message` | body | `string` | yes | Task description for the AI agent. |
| `provider` | body | `string` | no | AI provider to use. Accepted values: `0`, `1`, `2`. |
| `model` | body | `string` | no | Provider-specific model name. |
| `createBranch` | body | `boolean` | no | Create a git branch for the changes. |
| `createPR` | body | `boolean` | no | Create a pull request after completion. |
| `githubToken` | body | `string` | no | GitHub token for private repositories or pull request creation. |
