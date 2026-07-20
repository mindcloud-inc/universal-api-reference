# Get Target with Snyk

Retrieves a target from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/targets/:target_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Target](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | Snyk target ID for the request path. |
