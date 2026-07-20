# Update Event with VSCO Workspace

Updates an existing event in VSCO Workspace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/event/:id`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Update Event](https://workspace.vsco.co/api/#operation/updateResourceEvent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `allDay` | body | `boolean` | no | — |
| `channel` | body | `string` | no | — |
| `confirmed` | body | `boolean` | no | — |
| `descriptionHtml` | body | `string` | no | — |
| `endDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `endTime` | body | `string` | no | A time string using 24-hour format (seconds are ignored) |
| `endUtc` | body | `object` | no | — |
| `galleryId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `jobId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `location` | body | `object` | no | — |
| `name` | body | `string` | no | — |
| `phoneNumber` | body | `object` | no | — |
| `startDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `startTime` | body | `string` | no | A time string using 24-hour format (seconds are ignored) |
| `startUtc` | body | `object` | no | — |
| `timezoneName` | body | `string` | no | A VSCO Workspace approved timezone name. If `timezoneId` is provided then this will be ignored. |
| `timezoneId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `typeId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `virtualUrl` | body | `string` | no | — |
