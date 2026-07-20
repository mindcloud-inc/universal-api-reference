# List Repositories in Workspace with Bitbucket

Retrieves repositories from a Bitbucket workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Repositories in Workspace](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | no | Workspace slug. |
