# Delete File with GitHub

Deletes a file from a GitHub repository.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/repos/:owner/:repo/contents/:path`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Delete File](https://docs.github.com/en/rest/repos/contents#delete-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `path` | path | `string` | yes | Path to the file within the repository. |
| `message` | body | `string` | yes | The commit message. |
| `sha` | body | `string` | yes | The blob SHA of the file being deleted. |
| `branch` | body | `string` | no | The branch name. Defaults to the repository default branch. |
| `committer` | body | `object` | no | Committer information. |
| `committer.name` | body | `string` | no | The name of the committer. |
| `committer.email` | body | `string` | no | The email of the committer. |
| `author` | body | `object` | no | Author information. |
| `author.name` | body | `string` | no | The name of the author. |
| `author.email` | body | `string` | no | The email of the author. |
