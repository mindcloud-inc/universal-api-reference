# List Events with GoodDay.work

Finds events in the GoodDay.work workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List Events](https://www.goodday.work/developers/api-v2/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Events start date in YYYY-MM-DD. |
| `endDate` | query | `string` | yes | Events end date in YYYY-MM-DD. |
| `eventTypes` | query | `string` | no | Comma-separated GoodDay event types. |
