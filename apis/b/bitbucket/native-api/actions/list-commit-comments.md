# List Commit Comments with Bitbucket

Retrieves commit comments from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/commit/:commit/comments`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Commit Comments](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repo_slug` | path | `string` | no | Repository slug. |
| `workspace` | path | `string` | no | Workspace slug. |
