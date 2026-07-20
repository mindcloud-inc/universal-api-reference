# List Devices with Persona

## Endpoint

- **Method:** `GET`
- **Path:** `/devices`
- **Base URL:** `https://api.withpersona.com/api/v1`
- **Official documentation:** [List Devices](https://docs.withpersona.com/api-reference/devices/list-all-devices)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[inquiry-session-id]` | query | `string` | yes | Filter devices by inquiry session ID |
