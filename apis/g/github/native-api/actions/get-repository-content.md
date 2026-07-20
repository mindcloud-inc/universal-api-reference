# Get Repository Content with GitHub

Retrieves repository content from GitHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/contents/:path`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Repository Content](https://docs.github.com/en/rest/repos/contents#get-repository-content)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.github.object+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `path` | path | `string` | yes | Specify the file path or directory path to retrieve. |
| `ref` | query | `string` | no | The name of the commit, branch, or tag. |
