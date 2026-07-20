# Get Group Export with Snyk

Retrieves an export from a Snyk group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/export/:export_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Group Export](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `export_id` | path | `string` | yes | Export ID for the request path. |
