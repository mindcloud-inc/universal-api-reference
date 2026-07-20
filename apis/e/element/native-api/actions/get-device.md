# Get Device with Element

Retrieves a device from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/devices/:deviceId`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Device](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3devicesdeviceid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | Matrix device ID to retrieve. |
