# List Releases with GitHub Utils

Retrieves releases from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/releases`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Releases](https://docs.github.com/en/rest/releases/releases#list-releases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
