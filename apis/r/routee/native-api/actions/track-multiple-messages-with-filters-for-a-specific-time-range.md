# Track multiple messages with filters for a specific time range with Routee

Tracks multiple messages with filters for a specific time range in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/tracking`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track multiple messages with filters for a specific time range](https://docs.routee.net/reference/track-multiple-sms-with-filters-for-a-specific-time-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateStart` | query | `date` | yes | ISO-8601 date-time format (accept a date range only for the latest 7 days) |
| `dateEnd` | query | `date` | yes | ISO-8601 date-time format (accept a date range only for the latest 7 days) |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `trackingId` | query | `string` | no | If provided then only the SMS messages for the specific Campaign Tracking Id will be retrieved. |
| `campaign` | query | `boolean` | no | If true it will return only SMS messages that belong to an SMS campaign. |
| `fieldName` | body | `string` | yes | The name of the field to filter. Available values: smsId, to, status.status, direction, label, campaign |
| `searchTerm` | body | `string` | yes | The exact value that the specified field must match. |
| `searchOperator` | body | `string` | no | Optional: The operator upon which the search operation will be executed. Possible values: 'is', 'is_not', 'contains', 'starts_with', 'ends_with'. If missing defaults to 'is'. |
