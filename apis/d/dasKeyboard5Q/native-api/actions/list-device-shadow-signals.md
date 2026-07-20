# List Device Shadow Signals with Das Keyboard 5Q

Retrieves shadow signals for a device from Das Keyboard 5Q.

## Endpoint

- **Method:** `GET`
- **Path:** `/signals/pid/:pid/shadows`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [List Device Shadow Signals](https://www.daskeyboard.io/api-ressources/signal/get-shadow-signals-for-device/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pid` | path | `string` | yes | PID of the device whose shadow signals should be fetched. |
