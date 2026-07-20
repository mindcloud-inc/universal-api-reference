# List Branches with GitHub Utils

Retrieves branches from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/branches`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Branches](https://docs.github.com/en/rest/branches/branches#list-branches)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
