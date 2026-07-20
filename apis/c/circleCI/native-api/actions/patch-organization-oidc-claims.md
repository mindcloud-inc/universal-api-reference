# Patch Organization OIDC Claims with CircleCI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/org/:orgID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Patch Organization OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/PatchOrgClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | The CircleCI organization UUID. |
| `ttl` | body | `string` | no | OIDC token TTL duration. |
