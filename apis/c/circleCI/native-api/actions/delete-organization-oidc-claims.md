# Delete Organization OIDC Claims with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/org/:orgID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Organization OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/DeleteOrgClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `claims` | query | `string` | yes | Comma-separated claim names to delete. |
| `orgID` | path | `string` | yes | The CircleCI organization UUID. |
