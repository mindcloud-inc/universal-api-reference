# Create Issue with GitHub Utils

Creates a new issue on GitHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/issues`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Issue](https://docs.github.com/en/rest/issues/issues#create-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | The issue body. |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `title` | body | `string` | yes | The title of the issue. |
