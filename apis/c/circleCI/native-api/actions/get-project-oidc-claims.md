# Get Project OIDC Claims with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/org/:orgID/project/:projectID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/GetProjectClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | no | Opaque organization identifier. |
| `projectID` | path | `string` | no | Opaque project identifier. |
