# List Version Items with Rollbar

Retrieves version items from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/versions/:version/items`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [List Version Items](https://docs.rollbar.com/reference/get_api-1-versions-version-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `version` | path | `string` | yes | Code version string |
