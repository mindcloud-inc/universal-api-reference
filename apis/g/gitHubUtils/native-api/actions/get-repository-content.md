# Get Repository Content with GitHub Utils

Retrieves repository content from GitHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/contents/:path`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Repository Content](https://docs.github.com/en/rest/repos/contents#get-repository-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `path` | path | `string` | yes | File or directory path in the repository. |
