# Start Workflow with Docubee

Starts a workflow in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflowTemplates/:templateId`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Start Workflow](https://docs.docubee.app/#start-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | The workflow start payload. |
| `templateId` | path | `string` | no | The workflow template ID. |
