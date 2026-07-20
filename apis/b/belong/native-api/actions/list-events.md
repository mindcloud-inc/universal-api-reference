# List Events with Belong

Retrieves all available events from Belong.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.belong.net/api/v3`
- **Official documentation:** [List Events](https://api.belong.net/api/v3/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hubId` | query | `string` | no | Filter events by hub ID. |
| `category[]` | query | `array<string>` | no | Filter events by category. Send multiple values as a string separated by `,`. |
| `online` | query | `boolean` | no | Filter for online events. |
| `private` | query | `boolean` | no | Filter for private events. |
| `start` | query | `date` | no | Return events intersecting this start time. |
| `end` | query | `date` | no | Return events intersecting this end time. |
| `search` | query | `string` | no | Search events. |
| `sort` | query | `list` | no | Sort field. Accepted values: `Created At`, `Updated At`. |
| `order` | query | `list` | no | Sort direction. Accepted values: `Ascending`, `Descending`. |
| `fields[]` | query | `array<string>` | no | Restrict returned fields. Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | 1-based page number. |
| `limit` | query | `number` | no | Items per page. |
| `cursor` | query | `string` | no | Cursor from the previous page. |
