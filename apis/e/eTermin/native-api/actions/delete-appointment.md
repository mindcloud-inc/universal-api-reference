# Delete Appointment with eTermin

Deletes an existing appointment from eTermin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/appointment`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Delete Appointment](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/delete_api_appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appid` | query | `number` | no | AppID of the appointment (relates to the ID) |
| `id` | query | `string` | no | ID of the appointment, <b>use externalid instead, if you use the parameter sync=1 or sendemail=1</b> (relates to the ExternalID) |
| `start` | query | `string` | no | Start date of the appointments. |
| `end` | query | `string` | no | End date of the appointments. |
| `sync` | query | `boolean` | no | True if the appointment should be synchronized with external calendars (use externalid instead of id Parameter) |
| `sendemail` | query | `boolean` | no | True if an email should be sent to the customer (use externalid instead of id Parameter) |
| `msgtype` | query | `number` | no | Defines which template should be sent |
