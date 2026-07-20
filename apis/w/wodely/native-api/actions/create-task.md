# Create Task with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Create Task](https://app.wodely.com/doc/api-documentation.html#create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskTypeId` | body | `number` | yes | Task type: 1 Delivery, 2 Pickup, 3 Appointment, 4 Field Workforce, 5 In-store Pickup, 6 Curbside Pickup, 7 Drive-thru Pickup. |
| `destinationAddress` | body | `string` | yes | Full destination address for geocoding. |
| `taskDesc` | body | `string` | no | Short task description. |
| `externalKey` | body | `string` | no | External order ID or barcode. |
| `alert` | body | `string` | no | Set `N` to disable email and SMS notifications. |
| `afterDateTime` | body | `string` | no | Complete-after time in UTC ISO 8601. |
| `beforeDateTime` | body | `string` | no | Complete-before time in UTC ISO 8601. |
| `requesterName` | body | `string` | no | Requester or sender name. |
| `recipientName` | body | `string` | no | Destination recipient name. |
| `recipientPhone` | body | `string` | no | Destination recipient phone number. |
