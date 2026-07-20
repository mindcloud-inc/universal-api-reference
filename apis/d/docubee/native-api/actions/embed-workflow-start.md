# Embed Workflow Start with Docubee

Creates an embedded workflow start session in Docubee.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Embed Workflow Start](https://docs.docubee.app/#embedded-workflow-start-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The whitelisted host domain for the embedded page. |
| `templateId` | body | `string` | no | The workflow template ID to start. |
