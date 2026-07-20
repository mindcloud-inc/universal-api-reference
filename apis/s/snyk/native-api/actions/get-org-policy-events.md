# List Organization Policy Events with Snyk

Retrieves policy events from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/policies/:policy_id/events`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Organization Policy Events](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Snyk policy ID for the request path. |
