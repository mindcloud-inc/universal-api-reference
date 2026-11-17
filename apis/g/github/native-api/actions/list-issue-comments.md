# List Issue Comments with GitHub

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/issues/:issue_number/comments`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Issue Comments](https://docs.github.com/en/rest/issues/comments#list-issue-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `issue_number` | path | `number` | yes | The number that identifies the issue or pull request. |
| `per_page` | query | `number` | no | The number of results per page (max 100). |
