# Create Issue Comment with GitHub

Creates an issue comment in GitHub.

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
| `issue_number` | path | `number` | yes | Issue or pull request number. |
| `body` | body | `string` | yes | The contents of the comment. |
