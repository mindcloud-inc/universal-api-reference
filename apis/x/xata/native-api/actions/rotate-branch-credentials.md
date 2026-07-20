# Rotate branch credentials with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/credentials/rotate`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Rotate branch credentials](https://xata.io/docs/api-reference/branches/rotate-branch-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | — |
| `projectID` | path | `string` | yes | — |
| `branchID` | path | `string` | yes | — |
| `username` | body | `string` | yes | Database username to rotate credentials for |
