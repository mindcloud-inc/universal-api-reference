# Get Rate Calendar with Lodgify

Retrieves a nightly rate calendar from Lodgify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/rates/calendar`
- **Base URL:** `https://api.lodgify.com`
- **Official documentation:** [Get Rate Calendar](https://docs.lodgify.com/reference/ratescalendar-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `HouseId` | query | `number` | yes | Property identifier from Lodgify. |
| `RoomTypeId` | query | `number` | yes | Room type identifier from Lodgify. |
| `StartDate` | query | `string` | yes | Start date for the rates calendar. |
| `EndDate` | query | `string` | yes | End date for the rates calendar. |
