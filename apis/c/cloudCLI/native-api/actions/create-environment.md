# Create Environment with Cloud CLI

Creates a new environment in Cloud CLI.

## Endpoint

- **Method:** `POST`
- **Path:** `/environments`
- **Base URL:** `https://cloudcli.ai/api/v1`
- **Official documentation:** [Create Environment](https://developer.cloudcli.ai/create-environment-3998768e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new environment. Maximum length: 50. |
| `subdomain` | body | `string` | yes | Unique subdomain slug for the environment. Maximum length: 30. |
| `github_url` | body | `string` | no | GitHub repository URL to clone into the environment. |
| `github_token` | body | `string` | no | GitHub personal access token for private repositories. |
