# Track multiple Number Lookup requests with filters with Routee

Tracks multiple number lookup requests with filters in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/lookup/tracking`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track multiple Number Lookup requests with filters](https://docs.routee.net/reference/track-multiple-hlr-lookup-records-with-filters-for-a-specific-time-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateStart` | query | `date` | no | ISO-8601 date-time format |
| `dateEnd` | query | `date` | no | ISO-8601 date-time format |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page) |
| `size` | query | `number` | no | The number of items to retrieve, default value is 10. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `fieldName` | body | `string` | yes | The name of the field to filter. Possible values: 'lookupID', 'network', 'label', 'country', 'status', 'ported', 'imsi', 'roaming', 'groups', 'campaignName', 'campaignID'. If a non-existed field name value is used then all the results are returned. |
| `searchTerm` | body | `string` | yes | The exact value that the specified field must match. |
| `searchOperator` | body | `string` | no | Optional: The operator upon which the search operation will be executed. Possible values: 'is', 'is_not', 'contains', 'starts_with', 'ends_with'. If missing defaults to 'is'. |
