# Get Event Details with Corsizio

Retrieves an event from Corsizio by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:id`
- **Base URL:** `https://api.corsizio.com/v1`
- **Official documentation:** [Get Event Details](https://help.corsizio.com/article/41-api-get-event-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | The event ID to request. |
| `include` | query | `list<string>` | no | Comma-separated values: filters, stats, attendees, payment. Accepted values: `attendees`, `filters`, `payment`, `stats`. Send multiple values as a string separated by `,`. |
| `expand` | query | `list<string>` | no | Comma-separated values: filters, instructors, account. Accepted values: `account`, `filters`, `instructors`. Send multiple values as a string separated by `,`. |
