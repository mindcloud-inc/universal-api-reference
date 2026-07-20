# Batch Revoke Credentials with Paradym

Revokes issued credentials in bulk in Paradym.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/revocation/batch`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [Batch Revoke Credentials](https://paradym.id/reference#tag/revocation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `issuedCredentialIds[0]` | body | `string` | yes |
| `issuedCredentialIds[1]` | body | `string` | no |
| `issuedCredentialIds[2]` | body | `string` | no |
