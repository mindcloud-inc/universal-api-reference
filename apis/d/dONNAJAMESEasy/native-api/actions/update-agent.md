# Update Agent with DONNAJAMES Easy

Updates an existing agent in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `agent/:uuid/update`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Update Agent](https://guide.gpt-trainer.com/api-reference/agents/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | — |
| `model` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `prompt` | body | `string` | no | — |
| `uuid` | path | `string` | yes | Agent uuid |
| `enabled` | body | `boolean` | no | — |
| `temperature` | body | `number` | no | — |
| `use_all_sources` | body | `boolean` | no | — |
