# List apps with Pipedream

Retrieves a list of apps from Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [List apps](https://pipedream.com/docs/rest-api/api-reference/apps/list-apps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `has_actions` | query | `string` | no | Pass `1` to only return apps with public actions. |
| `has_components` | query | `string` | no | Pass `1` to only return apps with public triggers or actions. |
| `has_triggers` | query | `string` | no | Pass `1` to only return apps with public triggers. |
| `q` | query | `string` | no | Optional query string to filter the list of apps. |
