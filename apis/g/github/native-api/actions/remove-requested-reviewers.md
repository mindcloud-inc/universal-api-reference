# Remove Requested Reviewers with GitHub

## Endpoint

- **Method:** `DELETE`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number/requested_reviewers`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Remove Requested Reviewers](https://docs.github.com/en/rest/pulls/review-requests#remove-requested-reviewers-from-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `pull_number` | path | `number` | yes | The number that identifies the pull request. |
| `reviewers[]` | body | `array<string>` | yes | User logins that will be removed as requested reviewers. |
| `team_reviewers[]` | body | `array<string>` | no | Team slugs that will be removed as requested reviewers. |
