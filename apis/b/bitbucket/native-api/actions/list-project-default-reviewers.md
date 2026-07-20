# List Project Default Reviewers with Bitbucket

Retrieves project default reviewers from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace/projects/:project_key/default-reviewers`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [List Project Default Reviewers](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-projects/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_key` | path | `string` | no | Project key. |
| `workspace` | path | `string` | no | Workspace slug. |
