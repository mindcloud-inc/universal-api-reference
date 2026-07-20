# Embed Workflow Runtime with Docubee

Creates an embedded workflow runtime session in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Embed Workflow Runtime](https://docs.docubee.app/#embedded-workflow-runtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The whitelisted host domain for the embedded page. |
| `instanceId` | body | `string` | no | The workflow instance ID to continue. |
| `participant` | body | `string` | no | The participant email or the literal value anonymous. |
