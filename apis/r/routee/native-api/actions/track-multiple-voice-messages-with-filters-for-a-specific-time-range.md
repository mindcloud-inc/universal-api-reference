# Track multiple voice messages with filters for a specific time range with Routee

Tracks multiple voice messages with filters for a specific time range in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/tracking`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track multiple voice messages with filters for a specific time range](https://docs.routee.net/reference/calltracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | ISO-8601 date-time format |
| `to` | query | `string` | no | ISO-8601 date-time format |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `trackingId` | query | `string` | no | If provided then only the voice messages of the campaign with this tracking Id will be retrieved. |
| `tagged` | query | `boolean` | no | — |
| `fieldName` | body | `string` | yes | Defines the name of the field for this filter. ACCEPTED VALUES: id, recipient, from, collectedTones, groups, country, status.status, campaign |
| `searchOperator` | body | `string` | no | Defines the search operator to be used for the search. Examples: is, is_not, contains, starts_with, ends_with |
| `searchTerm` | body | `string` | yes | Defines the value of the specified field. |
