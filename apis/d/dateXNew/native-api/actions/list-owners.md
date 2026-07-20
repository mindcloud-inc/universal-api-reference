# List Owners with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `owners/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Owners](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_owners_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.lookups[]` | body | `array<string>` | no | Owner lookup filters. |
| `filters.names[]` | body | `array<string>` | no | Owner name filters. |
| `filters.statuses[]` | body | `array<string>` | no | Owner status filters. |
| `filters.project.lookups[]` | body | `array<string>` | no | Project lookup filters. |
| `filters.project.names[]` | body | `array<string>` | no | Project name filters. |
| `filters.project.statuses[]` | body | `array<string>` | no | Project status filters. |
