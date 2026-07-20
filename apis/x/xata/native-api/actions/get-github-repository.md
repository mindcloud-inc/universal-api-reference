# Get GitHub repository for branch with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get GitHub repository for branch](https://xata.io/docs/api-reference/github-app/get-github-repository-for-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization |
| `projectID` | path | `string` | yes | Unique identifier of the project |
| `branchID` | path | `string` | yes | Unique identifier of the branch |
