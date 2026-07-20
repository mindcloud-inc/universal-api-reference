# Run Agent with PromptLayer Run Agent

Runs a PromptLayer workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_name/run`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Run Agent](https://docs.promptlayer.com/reference/run-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_name` | path | `string` | yes | Name of the PromptLayer agent to run. |
| `workflow_label_name` | body | `string` | no | Optional release label for the agent version to run. |
| `workflow_version_number` | body | `number` | no | Optional agent version number to run. |
| `metadata` | body | `object` | no | Optional metadata attached to this execution. |
| `input_variables` | body | `object` | no | Optional input variables for the agent execution. |
| `return_all_outputs` | body | `boolean` | no | Whether to return all output nodes instead of only the final output. |
| `callback_url` | body | `string` | no | Optional webhook URL for asynchronous completion delivery. |
