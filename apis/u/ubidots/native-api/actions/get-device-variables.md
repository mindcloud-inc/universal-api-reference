# Get Device Variables with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/:device_key/variables/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Device Variables](https://docs.ubidots.com/reference/get-all-variables)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_key` | path | `string` | yes | The device ID or API label. |
