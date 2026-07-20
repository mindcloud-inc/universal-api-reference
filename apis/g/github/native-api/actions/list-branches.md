# List Branches with GitHub

Lists branches in a GitHub repository.

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
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `protected` | query | `boolean` | no | Filter by whether the returned branches are protected. |
