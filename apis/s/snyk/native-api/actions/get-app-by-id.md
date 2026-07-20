# Get App By ID with Snyk

Retrieves a created app from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/apps/creations/:app_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get App By ID](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Snyk app ID for the request path. |
