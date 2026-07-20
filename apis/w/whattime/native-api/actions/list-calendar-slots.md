# List Calendar Slots with Whattime

## Endpoint

- **Method:** `GET`
- **Path:** `/reservation/calendars/:code/slots`
- **Base URL:** `https://api.whattime.co.kr/v1`
- **Official documentation:** [List Calendar Slots](https://developer.whattime.co.kr/swagger#/Calendar/reservationCalendarSlots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Resource Code |
| `date` | query | `date` | yes | — |
