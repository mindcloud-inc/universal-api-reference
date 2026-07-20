# Get Configuration Options with MantisBT

Retrieves configuration options from MantisBT by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/config`
- **Base URL:** `{baseUrl}/api/rest`
- **Official documentation:** [Get Configuration Options](https://github.com/mantisbt/mantisbt/blob/release-2.28.0/api/rest/mantisbt_openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `option[]` | query | `array<string>` | yes | One or more configuration option names to fetch Send multiple values as a array. |
