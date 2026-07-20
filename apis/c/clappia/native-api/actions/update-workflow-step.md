# Update Workflow Step with Clappia

Updates an existing workflow step in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflowdefinitionv2/updateWorkflowStep`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Workflow Step](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `triggerType` | body | `string` | yes | Workflow trigger type, such as newSubmission, editSubmission, or reviewSubmission. |
| `stepVariableName` | body | `string` | yes | Variable name of the existing workflow step to update. |
| `name` | body | `string` | no | Updated display name for the workflow step. |
| `instructions` | body | `string` | no | Updated node instructions, such as AI prompt text. |
| `model` | body | `string` | no | Updated model identifier for supported AI nodes. |
| `llm` | body | `string` | no | Updated LLM provider for supported AI nodes. |
