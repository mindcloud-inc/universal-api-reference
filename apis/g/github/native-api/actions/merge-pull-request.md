# Merge Pull Request with GitHub

Merges a pull request into the base branch in GitHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number/merge`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Merge Pull Request](https://docs.github.com/en/rest/pulls/pulls#merge-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `pull_number` | path | `number` | yes | Pull request number. |
| `commit_title` | body | `string` | no | Title for the automatic commit message. |
| `commit_message` | body | `string` | no | Extra detail to append to the automatic commit message. |
| `sha` | body | `string` | no | SHA that the pull request head must match to allow the merge. |
| `merge_method` | body | `list<string>` | no | The merge method to use. Accepted values: `0`, `1`, `2`. |
