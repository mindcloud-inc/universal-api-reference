# List Tags with Bitbucket

Retrieves tags from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/refs/tags`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Tags](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-refs/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | yes | Workspace slug. |
| `repo_slug` | path | `string` | yes | Repository slug. |
