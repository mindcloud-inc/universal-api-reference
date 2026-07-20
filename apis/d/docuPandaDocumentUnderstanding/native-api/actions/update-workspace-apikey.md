# Update Workspace Apikey with DocuPanda - Document Understanding

Updates a workspace API key in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/internal/workspace/update-apikey`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update Workspace Apikey](https://docs.docupipe.ai/openapi/docupipe.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newApiKey` | body | `string` | yes | New API key for the workspace |
| `workspaceOwnerId` | body | `string` | no | Owner ID if admin is updating another user |
