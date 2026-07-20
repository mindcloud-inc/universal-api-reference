# List Pull Requests with GitHub Utils

Retrieves pull requests from a GitHub repository.

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
| `state` | query | `string` | no | Pull request state to return. |
| `repo` | path | `string` | yes | Repository name. |
