# Get App By Client ID with Snyk

Retrieves an app from a Snyk organization by client ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/apps/:client_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get App By Client ID](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | Snyk client ID for the request path. |
