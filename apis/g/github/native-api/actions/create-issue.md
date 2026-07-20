# Create Issue with GitHub

Creates an issue in a GitHub repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/issues`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Issue](https://docs.github.com/en/rest/issues/issues#create-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `title` | body | `string` | yes | The title of the issue. |
| `body` | body | `string` | no | The contents of the issue. |
| `assignee` | body | `string` | no | Login for the user that this issue should be assigned to. |
| `milestone` | body | `number` | no | The milestone number to associate with this issue. |
| `labels[]` | body | `array<string>` | no | Labels to associate with this issue. |
| `assignees[]` | body | `array<string>` | no | User logins to assign to this issue. |
| `type` | body | `string` | no | The issue type name to associate with this issue. |
