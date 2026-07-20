# List Pull Requests with GitHub

Lists pull requests in a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/pulls`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Pull Requests](https://docs.github.com/en/rest/pulls/pulls#list-pull-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `state` | query | `string` | no | Pull request state to return. Accepted values: `0`, `1`, `2`. |
