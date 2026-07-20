# Update Service Appointment with Zoho FSM

Updates an existing service appointment in Zoho FSM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Service_Appointments`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Update Service Appointment](https://www.zoho.com/fsm/developer/help/api/edit-service-appointment.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[0].Appointments_X_Services[].Contact.id` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].id` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].Name` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].Service_Line_Item.id` | body | `string` | yes | The service line item ID inside the appointment-service relationship. |
| `data[0].Appointments_X_Services[].Service_Task_Line_Item.id` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].SLI_Status` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].STLI_Status` | body | `string` | no | — |
| `data[0].Appointments_X_Services[].Work_Order.id` | body | `string` | no | — |
| `data[0].id` | body | `string` | yes | The unique ID of the record. |
| `data[0].Summary` | body | `string` | no | A summary for the service appointment. |
| `data[0].Appointments_X_Services[]` | body | `array<object>` | yes | Appointment-service relationship objects to update on the service appointment. |
