# Retrieve Sd-Jwt Vc Credential Template with Paradym

Retrieves an SD-JWT VC credential template from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/templates/credentials/sd-jwt-vc/:credentialTemplateId`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Retrieve Sd-Jwt Vc Credential Template](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentialTemplateId` | path | `string` | yes | The SD-JWT VC credential template ID. |
