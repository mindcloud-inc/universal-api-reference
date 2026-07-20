# Get Encrypted Credentials with Seqera

Retrieves encrypted credential keys from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/credentials/:credentialsId/keys`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [Get Encrypted Credentials](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `credentialsId` | path | `string` | yes |
| `pairingId` | query | `string` | no |
| `workspaceId` | query | `string` | no |
