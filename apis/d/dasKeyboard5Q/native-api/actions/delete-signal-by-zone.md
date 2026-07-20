# Delete Signal By Zone with Das Keyboard 5Q

Deletes a signal by zone ID from Das Keyboard 5Q.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/signals/pid/:pid/zoneId/:zoneId`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [Delete Signal By Zone](https://www.daskeyboard.io/api-ressources/signal/delete-signal-by-zone-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pid` | path | `string` | yes | PID of the device whose zone signal should be deleted. |
| `zoneId` | path | `string` | yes | Keyboard zone whose signal should be deleted. |
