# List Appointments with CoachAccountable

Retrieves appointments from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Appointments](https://www.coachaccountable.com/APIDocs#Appointment.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Appointments by Client. |
| `CompanyID` | body | `number` | no | Filter Appointments by the Company that the Clients belong to. |
| `name` | body | `string` | no | Filter Appointments by name, supports partial matching on prefix. |
| `dateFrom` | body | `date` | no | Set to restrict Appointments returned to those starting at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Appointments returned to those starting at or before the provided value. |
| `includePending` | body | `boolean` | no | Set to true to include Appointments which are still just pending requests. |
| `includeCanceled` | body | `boolean` | no | Set to true to include Appointments that have been canceled. |
