# Get User with Snyk

Retrieves a user from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/users/:id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get User](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Snyk user ID for the request path. |
