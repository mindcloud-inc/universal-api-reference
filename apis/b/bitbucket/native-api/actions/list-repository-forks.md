# List Repository Forks with Bitbucket

Retrieves repository forks from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/forks`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Repository Forks](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repo_slug` | path | `string` | no | Repository slug. |
| `workspace` | path | `string` | no | Workspace slug. |
