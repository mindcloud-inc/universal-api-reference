# Clear Alarm with ThingsBoard

Clears an alarm in ThingsBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/alarm/:alarmId/clear`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [Clear Alarm](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/clearAlarm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alarmId` | path | `string` | yes | The ThingsBoard alarm ID. |
