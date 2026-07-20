# List Repository Workflows with GitHub

Lists workflows in a GitHub repository.

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
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
