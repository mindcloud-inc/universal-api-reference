# Get Repository with GitHub

Retrieves a repository from GitHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Repository](https://docs.github.com/en/rest/repos/repos#get-a-repository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
