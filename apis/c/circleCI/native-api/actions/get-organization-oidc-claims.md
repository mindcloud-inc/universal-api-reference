# Get Organization OIDC Claims with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/org/:orgID/oidc-custom-claims`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Organization OIDC Claims](https://circleci.com/docs/api/v2/#tag/OIDC-Claims/operation/GetOrgClaims)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgID` | path | `string` | yes | The CircleCI organization UUID. |
