# List Related Assets with Snyk

Retrieves related assets from a Snyk asset.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/assets/:asset_id/relationships/assets`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Related Assets](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_id` | path | `string` | yes | Asset ID for the request path. |
