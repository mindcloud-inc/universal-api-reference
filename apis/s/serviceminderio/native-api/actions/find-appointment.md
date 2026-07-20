# Find Appointment with serviceminder.io

Retrieves an appointment from ServiceMinder by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/find`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Find Appointment](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AppointmentId` | body | `number` | yes | Appointment identifier. |
