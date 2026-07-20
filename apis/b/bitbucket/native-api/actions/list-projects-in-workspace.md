# List Projects in Workspace with Bitbucket

Retrieves projects from a Bitbucket workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace/projects`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Projects in Workspace](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | no | Workspace slug. |
