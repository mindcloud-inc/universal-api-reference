# Create Event with GoodDay.work

Creates a new event in GoodDay.work.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Create Event](https://www.goodday.work/developers/api-v2/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdByUserId` | body | `string` | yes | User ID on whose behalf the event is created. |
| `eventType` | body | `string` | yes | GoodDay event type. |
| `name` | body | `string` | yes | Event name. |
| `startDate` | body | `string` | yes | Event start date in YYYY-MM-DD. |
| `endDate` | body | `string` | no | Event end date in YYYY-MM-DD. |
| `projectId` | body | `string` | no | Project ID for project events. |
| `userId` | body | `string` | no | User ID for personal events. |
