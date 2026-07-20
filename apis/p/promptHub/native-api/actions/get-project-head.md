# Get Project Head with PromptHub

Retrieves a PromptHub project's head revision.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/head`
- **Base URL:** `https://app.prompthub.us/api/v1`
- **Official documentation:** [Get Project Head](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PromptHub project ID. |
| `branch` | query | `string` | no | Use the head revision from a specific branch. |
| `fallback` | query | `boolean` | no | When true, unspecified variables fall back to PromptHub defaults. |
