# Run Project with PromptHub

Runs a PromptHub project by project ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/run`
- **Base URL:** `https://app.prompthub.us/api/v1`
- **Official documentation:** [Run Project](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PromptHub project ID. |
| `branch` | body | `string` | no | Run the head revision from a specific branch. |
| `hash` | body | `string` | no | Run a specific project revision hash. |
| `variables` | body | `object` | no | Variable values to inject into the project request. |
| `prompt` | body | `string` | no | The final user message for chat projects. |
| `messages[]` | body | `array<object>` | no | Chat history messages for chat projects. |
| `metadata` | body | `object` | no | Metadata to associate with the PromptHub run. |
