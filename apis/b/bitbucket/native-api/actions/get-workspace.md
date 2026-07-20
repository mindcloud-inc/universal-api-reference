# Get Workspace with Bitbucket

Retrieves a workspace from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Workspace](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | yes | Workspace slug, for example mindcloudbitbucket20260409. |
