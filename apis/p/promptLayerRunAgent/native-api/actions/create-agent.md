# Create Agent with PromptLayer Run Agent

Creates a new workflow in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/workflows`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Agent](https://docs.promptlayer.com/reference/create-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new PromptLayer agent. |
| `nodes[]` | body | `array<object>` | yes | Workflow nodes array for the new agent. |
| `commit_message` | body | `string` | no | Message describing this agent version. |
| `required_input_variables` | body | `object` | no | Optional input variable map keyed by variable name. |
| `edges[]` | body | `array<object>` | no | Optional conditional edge definitions. |
| `release_labels[]` | body | `array<string>` | no | Optional release labels to attach to the created version. |
