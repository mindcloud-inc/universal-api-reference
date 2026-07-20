# Create or Update File Content with GitHub

Creates or updates a file in a GitHub repository.

## Endpoint

- **Method:** `PUT`
- **Path:** `/repos/:owner/:repo/contents/:path`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create or Update File Content](https://docs.github.com/en/rest/repos/contents#create-or-update-file-contents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `path` | path | `string` | yes | Path to the file within the repository. |
| `message` | body | `string` | yes | The commit message. |
| `content` | body | `string` | yes | The new file content, using Base64 encoding. |
| `sha` | body | `string` | no | The blob SHA of the file being replaced when updating an existing file. |
| `branch` | body | `string` | no | The branch name. Defaults to the repository default branch. |
| `committer` | body | `object` | no | Committer information. Defaults to the authenticated user. |
| `committer.name` | body | `string` | no | The name of the committer. |
| `committer.email` | body | `string` | no | The email of the committer. |
| `committer.date` | body | `date` | no | The commit date for the committer. |
| `author` | body | `object` | no | Author information. Defaults to the committer or authenticated user. |
| `author.name` | body | `string` | no | The name of the author. |
| `author.email` | body | `string` | no | The email of the author. |
| `author.date` | body | `date` | no | The commit date for the author. |
