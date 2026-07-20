# Create Maintenance with Instatus

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:page_id/maintenances`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Create Maintenance](https://instatus.com/help/api/maintenances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Maintenance name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `message` | body | `string` | no | Maintenance message. |
| `start` | body | `string` | yes | Maintenance start time. |
| `end` | body | `string` | yes | Maintenance end time. |
| `status` | body | `string` | yes | Maintenance status, such as NOTSTARTEDYET, INPROGRESS, or COMPLETED. |
| `notify` | body | `boolean` | yes | Whether to notify subscribers. |
| `components[]` | body | `array<string>` | yes | Affected component IDs. Send multiple values as a array. |
| `autoStart` | body | `boolean` | yes | Whether Instatus should automatically start the maintenance at the start time. |
| `autoEnd` | body | `boolean` | yes | Whether Instatus should automatically end the maintenance at the end time. |
| `notifyStart` | body | `boolean` | yes | Whether to notify subscribers when maintenance starts. |
| `notifyEnd` | body | `boolean` | yes | Whether to notify subscribers when maintenance ends. |
| `notifyEarly` | body | `boolean` | yes | Whether to notify subscribers before maintenance starts. |
| `duration` | body | `number` | no | Maintenance duration in minutes. |
| `statuses[]` | body | `array<object>` | no | Statuses for each affected component. Include matching component IDs in Component IDs. Send multiple values as a array. |
