# Search failover trackings with Routee

Searches Routee for failover tracking records.

## Endpoint

- **Method:** `POST`
- **Path:** `/failover/tracking`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Search failover trackings](https://docs.routee.net/reference/track-multiple-failovers-with-filters-for-a-specific-time-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateStart` | query | `string` | no | Start of the time range (e.g. 2025-05-05T15:00Z). |
| `dateEnd` | query | `string` | no | End of the time range (e.g. 2025-07-25T19:00Z) |
| `size` | query | `number` | no | Page size. Default: 10. Must be ≥ 1. |
| `fieldName` | body | `string` | yes | Field to filter on. Values: type, to, status, terminationChannel |
| `searchOperator` | body | `string` | no | Operator. Default: **is**. Values: **is**, **is_not**; for **to** also **contains**, **starts_with**, **ends_with**. Case-insensitive. |
| `searchTerm` | body | `string` | yes | Value to compare. For **type** / **terminationChannel**: **Sms**, **Viber**, **Voice**. For **status**: **Queued**, **Succeeded**, **Failed**, **InProgress**. For **to**: any string. |
| `page` | query | `number` | no | Page index (0-based). Default: 0. |
