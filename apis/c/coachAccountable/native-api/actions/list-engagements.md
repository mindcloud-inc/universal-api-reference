# List Engagements with CoachAccountable

Retrieves engagements from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Engagements](https://www.coachaccountable.com/APIDocs#Engagement.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Engagements by Client. |
| `CompanyID` | body | `number` | no | Filter Engagements by Company. |
| `startDateFrom` | body | `date` | no | Set to restrict Engagements returned to those with a start date at or after the provided value. |
| `startDateTo` | body | `date` | no | Set to restrict Engagements returned to those with a start date at or before the provided value. |
| `endDateFrom` | body | `date` | no | Set to restrict Engagements returned to those with an end date at or after the provided value. |
| `endDateTo` | body | `date` | no | Set to restrict Engagements returned to those with an end date at or before the provided value. |
| `includeAppointments` | body | `boolean` | no | Set to true to include Appointments which count towards the Engagement. |
