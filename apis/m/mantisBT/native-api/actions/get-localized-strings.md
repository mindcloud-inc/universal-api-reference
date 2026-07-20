# Get Localized Strings with MantisBT

Retrieves localized strings from MantisBT by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/lang`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Localized Strings](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `string[]` | query | `array<string>` | yes | One or more localization string keys to fetch Send multiple values as a array. |
