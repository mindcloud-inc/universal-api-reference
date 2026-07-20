# Create Airmeet with Airmeet

Creates a new event in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Create Airmeet](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventName` | body | `string` | yes | Name of the Airmeet event. |
| `hostEmail` | body | `string` | yes | Email address of the Airmeet event host. |
| `shortDesc` | body | `string` | yes | Short description of the event. |
| `timing.endTime` | body | `number` | yes | Event end time as a Unix timestamp in milliseconds. |
| `timing.startTime` | body | `number` | yes | Event start time as a Unix timestamp in milliseconds. |
| `timing.timezone` | body | `string` | yes | Canonical time zone name for the event. |
