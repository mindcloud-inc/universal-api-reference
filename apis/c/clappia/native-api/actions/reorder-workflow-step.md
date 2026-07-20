# Reorder Workflow Step with Clappia

Updates workflow step order in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflowdefinitionv2/reorderWorkflowStep`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Reorder Workflow Step](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `triggerType` | body | `string` | yes | Workflow trigger type, such as newSubmission, editSubmission, or reviewSubmission. |
| `stepVariableName` | body | `string` | yes | Variable name of the workflow step being moved. |
| `parentVariableName` | body | `string` | yes | Variable name of the new parent workflow step. |
