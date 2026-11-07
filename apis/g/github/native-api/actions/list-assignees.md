# List Assignees with GitHub

Retrieves the users who can be assigned to issues in a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/assignees`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Assignees](https://docs.github.com/en/rest/issues/assignees#list-assignees)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
