# Create Service Appointment with Zoho FSM

Creates a new service appointment in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Service_Appointments`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Service Appointment](https://www.zoho.com/fsm/developer/help/api/create-service-appointment.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[0].$allow_overlapping` | body | `boolean` | no | — |
| `data[0].$Service_Resources[]` | body | `array<string>` | no | — |
| `data[0].$Service_Tasks_Line_Items[]` | body | `array<string>` | no | — |
| `data[0].Lead` | body | `string` | no | — |
| `data[0].Summary` | body | `string` | yes | A summary for the service appointment. |
| `data[0].Territory` | body | `string` | no | — |
| `data[0].Scheduled_Start_Date_Time` | body | `string` | yes | The scheduled start date time for the appointment. |
| `data[0].Scheduled_End_Date_Time` | body | `string` | yes | The scheduled end date time for the appointment. |
| `data[0].$Service_Line_Items[]` | body | `array<string>` | no | Service line item IDs to include in the appointment. |
