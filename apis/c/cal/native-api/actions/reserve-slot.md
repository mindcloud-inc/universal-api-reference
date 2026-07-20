# Reserve Slot with Cal.com

Creates a slot reservation in Cal.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/slots/reservations`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Reserve Slot](https://cal.com/docs/api-reference/v2/slots/reserve-a-slot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventTypeId` | body | `number` | yes | Event type ID for the slot reservation. |
| `slotStart` | body | `string` | yes | Slot start time in ISO 8601 UTC format. |
| `slotDuration` | body | `number` | no | Reserved slot duration in minutes. |
| `reservationDuration` | body | `number` | no | Reservation hold duration in minutes. |
