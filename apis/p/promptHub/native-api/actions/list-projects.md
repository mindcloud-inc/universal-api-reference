# List Projects with PromptHub

Retrieves projects for a PromptHub team.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/projects`
- **Base URL:** `https://app.prompthub.us/api/v1`
- **Official documentation:** [List Projects](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PromptHub team ID. |
| `group` | query | `string` | no | Filter projects by group name. |
| `model` | query | `string` | no | Filter projects by the head model name. |
| `provider` | query | `string` | no | Filter projects by provider. |
