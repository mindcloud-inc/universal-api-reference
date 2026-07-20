# List Repository Webhooks with Bitbucket

Retrieves repository webhooks from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/hooks`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Repository Webhooks](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repo_slug` | path | `string` | no | Repository slug. |
| `workspace` | path | `string` | no | Workspace slug. |
