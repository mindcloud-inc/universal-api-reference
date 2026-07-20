# List Commits with GitHub

Lists commits in a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/commits`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Commits](https://docs.github.com/en/rest/commits/commits#list-commits)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `sha` | query | `string` | no | SHA or branch to start listing commits from. |
| `path` | query | `string` | no | Only commits containing this file path will be returned. |
| `author` | query | `string` | no | GitHub username or email address to use to filter by commit author. |
| `committer` | query | `string` | no | GitHub username or email address to use to filter by commit committer. |
| `since` | query | `string` | no | Only show results after this ISO 8601 timestamp. |
| `until` | query | `string` | no | Only show results before this ISO 8601 timestamp. |
