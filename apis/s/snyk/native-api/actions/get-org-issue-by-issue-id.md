# Get Organization Issue with Snyk

Retrieves an issue from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/issues/:issue_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Organization Issue](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `string` | yes | Snyk issue ID for the request path. |
