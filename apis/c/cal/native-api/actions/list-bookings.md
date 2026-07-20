# List Bookings with Cal.com

Retrieves bookings from Cal.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [List Bookings](https://cal.com/docs/api-reference/v2/bookings/get-all-bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list` | no | Filter bookings by status. Accepted values: `cancelled`, `past`, `recurring`, `rescheduled`, `unconfirmed`, `upcoming`. |
| `attendeeEmail` | query | `string` | no | Filter by attendee email. |
| `attendeeName` | query | `string` | no | Filter by attendee name. |
| `bookingUid` | query | `list` | no | Filter by booking UID. |
| `eventTypeId` | query | `list` | no | Filter by one event type ID. |
| `eventTypeIds` | query | `string` | no | Comma-separated event type IDs. |
| `teamId` | query | `string` | no | Filter by one team ID. |
| `teamsIds` | query | `string` | no | Comma-separated team IDs. |
| `afterStart` | query | `string` | no | Filter bookings with start after this ISO datetime. |
| `beforeEnd` | query | `string` | no | Filter bookings with end before this ISO datetime. |
| `afterCreatedAt` | query | `string` | no | Filter bookings created after this ISO datetime. |
| `beforeCreatedAt` | query | `string` | no | Filter bookings created before this ISO datetime. |
| `afterUpdatedAt` | query | `string` | no | Filter bookings updated after this ISO datetime. |
| `beforeUpdatedAt` | query | `string` | no | Filter bookings updated before this ISO datetime. |
| `sortStart` | query | `list` | no | Sort by start time (`asc` or `desc`). Accepted values: `asc`, `desc`. |
| `sortEnd` | query | `list` | no | Sort by end time (`asc` or `desc`). Accepted values: `asc`, `desc`. |
| `sortCreated` | query | `list` | no | Sort by creation time (`asc` or `desc`). Accepted values: `asc`, `desc`. |
| `sortUpdatedAt` | query | `list` | no | Sort by update time (`asc` or `desc`). Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | Number of bookings to return. |
| `skip` | query | `number` | no | Number of bookings to skip. |
