# Get Issue with GitHub

Retrieves an issue from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/issues/:issue_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Issue](https://docs.github.com/en/rest/issues/issues#get-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `issue_number` | path | `number` | yes | Issue number. |
