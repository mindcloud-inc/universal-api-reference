# Get Group Asset Filter Values with Snyk

Retrieves asset filter values from a Snyk group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/inventory/assets/filters/:filter_id/values`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Group Asset Filter Values](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_id` | path | `string` | yes | Filter field ID for the request path. |
