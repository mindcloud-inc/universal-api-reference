# Delete Project OIDC Claims with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/org/:orgID/project/:projectID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Project OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/DeleteProjectClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | no | Opaque organization identifier. |
| `projectID` | path | `string` | no | Opaque project identifier. |
