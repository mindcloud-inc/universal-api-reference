# Search Assets with Active Network

Finds activity assets in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/search`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Search Assets](https://developer.active.com/docs/read/v2_Activity_API_Search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Restrict results to one ACTIVE category. |
| `lat_lon` | query | `string` | no | Latitude and longitude separated by a comma. |
| `near` | query | `string` | no | Place name to geocode, such as City, State, Country. |
| `query` | query | `string` | no | Keywords to search across ACTIVE assets. |
| `radius` | query | `number` | no | Search radius around the provided near or lat/lon location. |
| `start_date` | query | `string` | no | Start-date range in yyyy-mm-dd..yyyy-mm-dd format. |
| `topicName` | query | `string` | no | Restrict results to one or more topic names. |
