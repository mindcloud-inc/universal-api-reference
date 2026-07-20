# Get Agent Execution Results with PromptLayer Run Agent

Retrieves execution results for a PromptLayer workflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow-version-execution-results`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Agent Execution Results](https://docs.promptlayer.com/reference/workflow-version-execution-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_version_execution_id` | query | `number` | yes | The PromptLayer workflow execution ID returned by `Run Agent`. |
| `return_all_outputs` | query | `boolean` | no | Whether to return all output nodes instead of only the main output. |
