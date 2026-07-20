# Patch Project OIDC Claims with CircleCI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/org/:orgID/project/:projectID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Patch Project OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/PatchProjectClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | body | `string` | no | OIDC audience value. |
| `orgID` | path | `string` | no | Opaque organization identifier. |
| `projectID` | path | `string` | no | Opaque project identifier. |
| `ttl` | body | `number` | no | OIDC token TTL in seconds. |
