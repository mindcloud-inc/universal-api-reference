# List Commits with GitHub Utils

Retrieves commits from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/commits`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Commits](https://docs.github.com/en/rest/commits/commits#list-commits)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
