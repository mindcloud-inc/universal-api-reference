# Get Repository Webhook with Bitbucket

Retrieves a repository webhook from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/hooks/:uid`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Repository Webhook](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repo_slug` | path | `string` | no | Repository slug. |
| `uid` | path | `string` | no | Webhook identifier. |
| `workspace` | path | `string` | no | Workspace slug. |
