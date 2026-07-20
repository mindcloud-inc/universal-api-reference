# Get Repository Settings Inheritance with Bitbucket

Retrieves repository settings inheritance from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/override-settings`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Repository Settings Inheritance](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repo_slug` | path | `string` | no | Repository slug. |
| `workspace` | path | `string` | no | Workspace slug. |
