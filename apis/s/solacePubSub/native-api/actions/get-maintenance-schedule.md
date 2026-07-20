# Get Maintenance Schedule with Solace PubSub+

Retrieves a maintenance schedule from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/missionControl/maintenanceSchedules/{maintenanceScheduleId}`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get Maintenance Schedule](https://api.solace.dev/cloud/reference/getmaintenanceschedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maintenanceScheduleId` | path | `string` | yes | Maintenance schedule identifier. |
