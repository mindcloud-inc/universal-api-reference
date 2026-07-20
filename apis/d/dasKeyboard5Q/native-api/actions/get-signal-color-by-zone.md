# Get Signal Color By Zone with Das Keyboard 5Q

Retrieves a signal color by zone ID from Das Keyboard 5Q.

## Endpoint

- **Method:** `GET`
- **Path:** `/signals/pid/:pid/zoneId/:zoneId/color`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [Get Signal Color By Zone](https://www.daskeyboard.io/api-ressources/signal/get-signal-color-by-zone-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pid` | path | `string` | yes | PID of the device to inspect. |
| `zoneId` | path | `string` | yes | Keyboard zone whose current color should be fetched. |
