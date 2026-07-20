# Get Organization Project with Snyk

Retrieves an organization project from Snyk.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/projects/:project_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Organization Project](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Snyk project ID for the request path. |
