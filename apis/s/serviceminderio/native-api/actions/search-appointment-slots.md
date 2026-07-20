# Search Appointment Slots with serviceminder.io

Finds appointment slots in ServiceMinder by date range and service.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/slotsearch`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Search Appointment Slots](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StartDate` | body | `date` | no | Slot-search start date. |
| `FinishDate` | body | `date` | no | Slot-search finish date. |
| `ServiceId` | body | `number` | no | Service identifier for slot search. |
