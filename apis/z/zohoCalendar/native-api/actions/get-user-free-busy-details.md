# Get User Free Busy Details with Zoho Calendar

Retrieves user free/busy details from Zoho Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/freebusy`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Get User Free Busy Details](https://www.zoho.com/calendar/help/api/get-user-freebusy-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uemail` | query | `string` | yes | Email address of the user whose free/busy details you want. |
| `sdate` | query | `string` | yes | Start datetime in yyyyMMdd'T'HHmmss format. |
| `edate` | query | `string` | yes | End datetime in yyyyMMdd'T'HHmmss format. |
| `ftype` | query | `string` | no | Free/busy response style, for example eventbased or timebased. |
