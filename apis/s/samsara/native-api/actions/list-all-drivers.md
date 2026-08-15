# List Drivers with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `fleet/drivers`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [List Drivers](https://developers.samsara.com/reference/listdrivers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driverActivationStatus` | query | `string` | no | Filter drivers by active or deactivated status. |
| `createdAfterTime` | query | `string` | no | Return drivers created at or after this RFC 3339 timestamp. |
| `updatedAfterTime` | query | `string` | no | Return drivers updated at or after this RFC 3339 timestamp. |
