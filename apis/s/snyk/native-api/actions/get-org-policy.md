# Get Organization Policy with Snyk

Retrieves a policy from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/policies/:policy_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Organization Policy](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Snyk policy ID for the request path. |
