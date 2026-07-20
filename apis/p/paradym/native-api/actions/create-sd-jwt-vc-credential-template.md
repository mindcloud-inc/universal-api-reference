# Create Sd-Jwt Vc Credential Template with Paradym

Creates an SD-JWT VC credential template in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/templates/credentials/sd-jwt-vc`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Create Sd-Jwt Vc Credential Template](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `type` | body | `string` | yes | Unique SD-JWT VC type label for the credential template. |
| `revocable` | body | `boolean` | yes | Whether credentials issued from this template can be revoked later. |
