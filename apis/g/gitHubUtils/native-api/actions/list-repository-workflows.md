# List Repository Workflows with GitHub Utils

Retrieves workflows from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/actions/workflows`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Repository Workflows](https://docs.github.com/en/rest/actions/workflows#list-repository-workflows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
