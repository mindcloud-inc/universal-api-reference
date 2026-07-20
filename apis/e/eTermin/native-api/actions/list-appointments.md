# List Appointments with eTermin

Retrieves appointments from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/appointment`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Appointments](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/get_api_appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appid` | query | `number` | no | ID of an appointment. (relates to the ID) |
| `id` | query | `string` | no | ID of an appointment. (relates to the ExternalID) |
| `start` | query | `string` | no | Start date of the appointments. Format yyyy-mm-dd. It will return a list with all appointments that are between "start" and "end". |
| `end` | query | `string` | no | End date of the appointments. Format yyyy-mm-dd. It will return a list with all appointments that are between "start" and "end". |
| `bycreationdate` | query | `boolean` | no | Changes the start and end parameters to look for the creation date instead of the date, the appointment takes place |
| `calendarid` | query | `string` | no | IDs of the calendars that you want to get appointments from, you can separate multiple calendars with a "," |
| `wl` | query | `boolean` | no | Set to 1 if you want to get all appointments on the Waiting List (start and end parameters required) |
| `pbl` | query | `boolean` | no | Set to 1 if you want to get all appointments on the Reservation List (start and end parameters not required) |
| `cid` | query | `number` | no | Use a customer ID to see all appointments that are related to this customer. (start and end parameters not required) |
| `email` | query | `string` | no | Use an email address to see all appointments that are related to this email. (start and end parameters required) |
| `limited` | query | `boolean` | no | Reduces the amount of information that the response have. Set to 1 if you want basic information about a lot of appointments. |
| `noholidays` | query | `boolean` | no | Only shows appointments that are no holidays and not blocked appointments. |
| `noholidays2` | query | `boolean` | no | Only shows appointments that are no holidays. (bookingtype <> "Holiday") |
