# Create a New Workflow Step with Linkbreakers

Creates a new workflow step in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/links/:linkId/workflow-steps`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create a New Workflow Step](https://linkbreakers.com/help/api/workflow-steps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | The ID of the link to create the workflow step for. |
| `canvasPosition` | body | `object` | no | Canvas position for the workflow step node. |
| `eventAction` | body | `string` | no | The event action type for the workflow step. |
| `id` | body | `string` | no | Optional workflow step ID. |
| `payload` | body | `object` | no | Workflow step payload. |
