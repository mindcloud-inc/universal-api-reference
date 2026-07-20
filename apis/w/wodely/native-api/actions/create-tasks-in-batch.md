# Create Tasks in Batch with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/bulkcreate`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Create Tasks in Batch](https://app.wodely.com/doc/api-documentation.html#create-task-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks[].taskTypeId` | body | `number` | yes | 1: Delivery; 2: Pickup; 3: Appointment; 4: Field Workforce; 5: In-store Pickup; 6: Curbside Pickup; 7: Drive-thru Pickup. |
| `tasks[].destinationAddress` | body | `string` | yes | Full delivery destination address. |
| `tasks[].taskDesc` | body | `string` | no | Short description of the task. |
| `tasks[].externalKey` | body | `string` | no | External order Id or barcode. |
| `tasks[].alert` | body | `string` | no | Set to N to disable notifications. |
| `tasks[].afterDateTime` | body | `string` | no | Complete after time in UTC ISO 8601. |
| `tasks[].beforeDateTime` | body | `string` | no | Complete before time in UTC ISO 8601. |
| `tasks[].requesterName` | body | `string` | no | Requester or sender name. |
| `tasks[].recipientName` | body | `string` | no | Destination recipient name. |
| `tasks[].recipientPhone` | body | `string` | no | Destination recipient phone. |
