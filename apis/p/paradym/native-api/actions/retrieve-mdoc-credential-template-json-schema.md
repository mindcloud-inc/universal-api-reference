# Retrieve Mdoc Credential Template JSON Schema with Paradym

Retrieves an mdoc credential template JSON schema from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/templates/credentials/mdoc/:credentialTemplateId/json-schema`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Retrieve Mdoc Credential Template JSON Schema](https://paradym.id/reference#tag/mdoc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialTemplateId` | path | `string` | yes | Template to inspect. |
