# List Repository Issues with GitHub

Lists issues in a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/issues`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Repository Issues](https://docs.github.com/en/rest/issues/issues#list-repository-issues)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `state` | query | `string` | no | Issue state to return. Accepted values: `0`, `1`, `2`. |
