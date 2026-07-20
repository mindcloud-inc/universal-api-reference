# List Service Calendars with eTermin

Retrieves calendars assigned to a service in eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/servicecalendar`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Service Calendars](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicecalendar/get_api_servicecalendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceid` | query | `string` | yes | ID of a service. Several service ID's can be separated with a comma (,). e.g. 45345,45346 etc. |
