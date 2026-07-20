# Start Workflow with Wrangle

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflowId/instances`
- **Base URL:** `https://slack.wrangle.io/api/v1`
- **Official documentation:** [Start Workflow](https://wrangle.apidocumentation.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | The Wrangle workflow ID to start. |
| `requesterId` | body | `string` | yes | The Slack user ID of the user starting the workflow instance. |
| `formFieldValues[]` | body | `array<object>` | yes | Workflow intake form values. |
