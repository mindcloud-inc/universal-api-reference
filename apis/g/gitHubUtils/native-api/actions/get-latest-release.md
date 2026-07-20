# Get Latest Release with GitHub Utils

Retrieves the latest release from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/releases/latest`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Latest Release](https://docs.github.com/en/rest/releases/releases#get-the-latest-release)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
