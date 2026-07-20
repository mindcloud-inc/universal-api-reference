# Update GitHub App installation with Xata

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:organizationID/githubapp/installations/:githubInstallationID`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Update GitHub App installation](https://xata.io/docs/api-reference/github-app/update-github-app-installation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization |
| `githubInstallationID` | path | `string` | yes | Unique identifier of the GitHub installation record |
| `installationId` | body | `number` | yes | GitHub App installation ID |
