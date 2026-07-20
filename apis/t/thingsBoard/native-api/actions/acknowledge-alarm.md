# Acknowledge Alarm with ThingsBoard

Acknowledges an alarm in ThingsBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/alarm/:alarmId/ack`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [Acknowledge Alarm](https://thingsboard.cloud/swagger-ui/index.html#/alarm-controller/ackAlarm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alarmId` | path | `string` | yes | The ThingsBoard alarm ID. |
