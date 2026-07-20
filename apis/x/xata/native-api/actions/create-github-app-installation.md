# Create GitHub App installation with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/githubapp/installations`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create GitHub App installation](https://xata.io/docs/api-reference/github-app/create-github-app-installation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization |
| `installationId` | body | `number` | yes | GitHub App installation ID |
