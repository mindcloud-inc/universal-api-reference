# List Contact Segments with Benchmark Email

Retrieves contact segments from Benchmark Email.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contact/Segments`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [List Contact Segments](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filter` | query | `string` | yes | Optional segment name filter. |
| `OrderBy` | query | `string` | yes | Segment sort column. |
| `PageNumber` | query | `string` | no | Optional page number for segment results. |
| `PageSize` | query | `string` | yes | Number of segment rows to return. |
| `SortOrder` | query | `string` | yes | Segment sort direction. |
