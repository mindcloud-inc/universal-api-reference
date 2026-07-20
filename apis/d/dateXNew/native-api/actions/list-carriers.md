# List Carriers with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `carriers/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Carriers](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_carriers_get)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.carrier_name` | body | `string` | no | Filter carriers by full carrier name. |
| `filters.carrier_short_name` | body | `string` | no | Filter carriers by short name. |
| `filters.scac` | body | `string` | no | Filter carriers by SCAC code. |
| `filters.carrier_id` | body | `number` | no | Filter carriers by numeric carrier ID. |
