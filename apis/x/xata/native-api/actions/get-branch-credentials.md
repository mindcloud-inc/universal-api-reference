# Retrieve branch credentials with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/credentials`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Retrieve branch credentials](https://xata.io/docs/api-reference/branches/retrieve-branch-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | — |
| `projectID` | path | `string` | yes | — |
| `branchID` | path | `string` | yes | — |
| `username` | query | `string` | no | Username that the credentials requested for |
