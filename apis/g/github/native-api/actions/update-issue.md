# Update Issue with GitHub

Updates an issue in a GitHub repository.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/repos/:owner/:repo/issues/:issue_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Update Issue](https://docs.github.com/en/rest/issues/issues#update-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `issue_number` | path | `number` | yes | Issue number. |
| `title` | body | `string` | no | The title of the issue. |
| `body` | body | `string` | no | The contents of the issue. |
| `assignee` | body | `string` | no | Username to assign to this issue. |
| `state` | body | `list<string>` | no | The open or closed state of the issue. Accepted values: `0`, `1`. |
| `state_reason` | body | `list<string>` | no | The reason for the state change. Accepted values: `0`, `1`, `2`, `3`. |
| `milestone` | body | `number` | no | The milestone number to associate with this issue. |
| `labels[]` | body | `array<string>` | no | Labels to associate with this issue. |
| `assignees[]` | body | `array<string>` | no | User logins to assign to this issue. |
| `type` | body | `string` | no | The issue type name to associate with this issue. |
