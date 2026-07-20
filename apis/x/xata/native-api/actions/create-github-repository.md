# Create GitHub repository mapping with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/githubapp/repository`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create GitHub repository mapping](https://xata.io/docs/api-reference/github-app/create-github-repository-mapping)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization |
| `projectID` | path | `string` | yes | Unique identifier of the project |
| `branchID` | path | `string` | yes | Unique identifier of the branch |
| `githubRepositoryID` | body | `number` | yes | GitHub repository ID |
