# List User Devices with Crexendo

Retrieves devices for a user in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/users/:user/devices`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List User Devices](https://docs.ns-api.com/reference/getdevices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | path | `string` | yes | User extension or identifier, for example 1000. |
