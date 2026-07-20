# Create Issue Comment with GitHub Utils

Creates an issue comment on GitHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/issues/:issue_number/comments`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Issue Comment](https://docs.github.com/en/rest/issues/comments#create-an-issue-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `issue_number` | path | `number` | yes | Issue number in the repository. |
| `body` | body | `string` | yes | The comment body. |
