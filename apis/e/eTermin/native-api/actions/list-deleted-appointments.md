# List Deleted Appointments with eTermin

Retrieves deleted appointments from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/appointmentdeleted`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Deleted Appointments](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/AppointmentDeleted/get_api_appointmentdeleted)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | no | Start day when appointment(s) got deleted. Format: yyyy-mm-dd. It will return a list with all appointments that are between start and end |
| `end` | query | `date` | no | End day when appointment(s) got deleted. Format: yyyy-mm-dd. It will return a list with all appointments there are between start and end |
