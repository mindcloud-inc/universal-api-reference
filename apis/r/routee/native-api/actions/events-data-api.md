# Events data API with Routee

Retrieves event data records from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/event`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Events data API](https://docs.routee.net/reference/events-data-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Object with data from event followed by the unique details of each event. |
| `uuid` | body | `string` | yes | authorization UUID ( Generated from WayMore authorization endpoint and will be provided after contact with the Tech Department) |
| `event` | body | `string` | yes | event name ex. CustomerAdd |
