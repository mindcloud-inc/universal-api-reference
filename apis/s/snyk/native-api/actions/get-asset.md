# Get Asset with Snyk

Retrieves an asset from a Snyk group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/assets/:asset_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Asset](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_id` | path | `string` | yes | Asset ID for the request path. |
