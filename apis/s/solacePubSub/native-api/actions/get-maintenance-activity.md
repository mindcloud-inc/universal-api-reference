# Get Maintenance Activity with Solace PubSub+

Retrieves a maintenance activity from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/missionControl/maintenanceActivities/{maintenanceActivityId}`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get Maintenance Activity](https://api.solace.dev/cloud/reference/getmaintenanceactivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maintenanceActivityId` | path | `string` | yes | Maintenance activity identifier. |
