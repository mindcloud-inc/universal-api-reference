# Import Workflow with Docubee

Imports a workflow into Docubee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflowTemplates/:templateId`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Import Workflow](https://docs.docubee.app/#import)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/docubee` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | The imported workflow template payload. |
| `fileContentBase64` | body | `string` | no | The exported workflow file content encoded as base64. |
| `publish` | query | `string` | no | Whether to publish the imported workflow immediately. Use true to make the template startable. |
| `templateId` | path | `string` | no | The workflow template ID. |
