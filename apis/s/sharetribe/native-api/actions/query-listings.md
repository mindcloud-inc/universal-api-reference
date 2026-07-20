# Query Listings with Sharetribe

Retrieves listings from Sharetribe.

## Endpoint

- **Method:** `GET`
- **Path:** `listings/query`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Query Listings](https://www.sharetribe.com/api-reference/integration.html#query-listings)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorId` | query | `string` | no | Match only listings belonging to this user ID. |
| `ids` | query | `string` | no | Comma-separated list of listing IDs to match, up to 100 IDs. Send multiple values as a string separated by `,`. |
| `states` | query | `string` | no | Comma-separated list of listing states to include. Send multiple values as a string separated by `,`. |
| `createdAtStart` | query | `date` | no | Filter listings created on or after this ISO 8601 timestamp. |
| `createdAtEnd` | query | `date` | no | Filter listings created before this ISO 8601 timestamp. |
| `keywords` | query | `string` | no | Keywords to match against listing title, description, and eligible public data text fields. |
| `origin` | query | `string` | no | Origin coordinates as latitude,longitude. Cannot be combined with keywords. |
| `bounds` | query | `string` | no | Bounding box coordinates as NE lat,NE lng,SW lat,SW lng. |
| `price` | query | `string` | no | Price filter using minor units. Supports VALUE, START,END, START, or ,END syntax. |
| `start` | query | `date` | no | Availability interval start time in ISO 8601 format. |
| `end` | query | `date` | no | Availability interval end time in ISO 8601 format. |
| `seats` | query | `number` | no | Minimum number of available seats required for the interval. |
| `availability` | query | `string` | no | Availability search type: day-full, day-partial, time-full, or time-partial. |
| `minDuration` | query | `number` | no | Minimum matching availability duration within the requested range. |
| `stockMode` | query | `string` | no | Stock query mode: strict or match-undefined. |
| `minStock` | query | `number` | no | Match listings whose current stock quantity is at least this value. |
