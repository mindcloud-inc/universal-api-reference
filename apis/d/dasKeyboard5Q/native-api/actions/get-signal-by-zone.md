# Get Signal By Zone with Das Keyboard 5Q

Retrieves a signal by zone ID from Das Keyboard 5Q.

## Endpoint

- **Method:** `GET`
- **Path:** `/signals/pid/:pid/zoneId/:zoneId`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [Get Signal By Zone](https://www.daskeyboard.io/api-ressources/signal/get-signal-by-zone-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pid` | path | `string` | yes | PID of the device to inspect. |
| `zoneId` | path | `string` | yes | Keyboard zone to inspect, such as KEY_Q, 74, or 2,2. |
