# Get Group Issue with Snyk

Retrieves an issue from a Snyk group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/issues/:issue_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Group Issue](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `string` | yes | Snyk issue ID for the request path. |
