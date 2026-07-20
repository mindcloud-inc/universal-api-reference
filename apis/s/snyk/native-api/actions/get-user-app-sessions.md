# List User App Sessions with Snyk

Retrieves app sessions for the current Snyk user.

## Endpoint

- **Method:** `GET`
- **Path:** `/self/apps/:app_id/sessions`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List User App Sessions](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Snyk app ID for the request path. |
