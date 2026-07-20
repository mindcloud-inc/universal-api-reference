# Create Workspace with DocuPanda - Document Understanding

Creates a new workspace in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/create`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Create Workspace](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `makeDefault` | body | `boolean` | no | If true, create/return the user's default workspace |
| `name` | body | `string` | no | Name of the new workspace |
