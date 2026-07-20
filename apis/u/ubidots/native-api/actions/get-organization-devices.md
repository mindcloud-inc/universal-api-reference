# Get Organization Devices with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_key/devices/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Organization Devices](https://docs.ubidots.com/reference/get-all-devices-of-organization)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_key` | path | `string` | yes | The organization ID or key. |
