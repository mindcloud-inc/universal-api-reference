# Update Maintenance with Instatus

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:page_id/maintenances/:maintenance_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Update Maintenance](https://instatus.com/help/api/maintenances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Maintenance name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `maintenance_id` | path | `string` | yes | Instatus maintenance ID. |
| `message` | body | `string` | yes | Message for the maintenance update. |
| `start` | body | `string` | yes | Maintenance start date and time. |
| `end` | body | `string` | yes | Maintenance end date and time. |
| `status` | body | `string` | yes | Maintenance status. |
| `notify` | body | `boolean` | yes | Whether to notify subscribers. |
| `components[]` | body | `array<string>` | yes | Affected component IDs. Send multiple values as a array. |
| `statuses[]` | body | `array<object>` | yes | Statuses for each affected component. Include matching component IDs in Component IDs. Send multiple values as a array. |
| `duration` | body | `number` | yes | Maintenance duration in minutes. |
| `autoStart` | body | `boolean` | yes | Whether Instatus should automatically start the maintenance at the start time. |
| `autoEnd` | body | `boolean` | yes | Whether Instatus should automatically end the maintenance at the end time. |
