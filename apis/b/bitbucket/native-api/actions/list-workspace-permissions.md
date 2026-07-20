# List Workspace Permissions with Bitbucket

Retrieves workspace permissions from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace/permissions`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Workspace Permissions](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | no | Workspace slug. |
