# Create Prompt Version with Statsig

Creates a prompt version in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/prompts/{id}/versions`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Prompt Version](https://docs.statsig.com/api-reference/prompts/create-prompt-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `prompts` | body | `list` | no | Request body field. |
| `temperature` | body | `number` | no | Request body field. |
| `model` | body | `string` | no | Request body field. |
| `name` | body | `string` | yes | Request body field. |
| `provider` | body | `string` | no | Request body field. |
| `workflow_body` | body | `object` | no | Request body field. |
| `workflow_headers` | body | `list` | no | Request body field. |
| `auth_workflow_headers` | body | `list` | no | Request body field. |
| `eval_model` | body | `string` | no | Request body field. |
| `top_p` | body | `number` | no | Request body field. |
| `frequency_penalty` | body | `number` | no | Request body field. |
| `presence_penalty` | body | `number` | no | Request body field. |
| `max_tokens` | body | `number` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
