# List Owners with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `owners/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Owners](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_owners_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters` | body | `object` | no |
| `filters.lookups[]` | body | `array<string>` | no |
| `filters.project.lookups[]` | body | `array<string>` | no |
| `filters.names[]` | body | `array<string>` | no |
| `filters.project.names[]` | body | `array<string>` | no |
| `filters.project.statuses[]` | body | `array<string>` | no |
| `filters.statuses[]` | body | `array<string>` | no |
| `filters.project` | body | `object` | no |
