# Retrieve Mdoc Credential Template with Paradym

Retrieves an mdoc credential template from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/templates/credentials/mdoc/:credentialTemplateId`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Retrieve Mdoc Credential Template](https://paradym.id/reference#tag/mdoc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialTemplateId` | path | `string` | yes | Template to retrieve. |
