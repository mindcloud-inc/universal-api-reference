# List Booked Meetings with Lemcal

Retrieves your booked meetings from Lemcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetings`
- **Base URL:** `https://api.lemcal.com/api/lemcal`
- **Official documentation:** [List Booked Meetings](https://developer.lemcal.com/#list-booked-meetings)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingTypeId` | query | `string` | no | Filter meetings by a specific meeting type ID. |
