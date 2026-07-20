# Search Kids Assets with Active Network

Finds kids activity assets in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/search`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Search Kids Assets](https://developer.active.com/docs/read/Kids_Activity_Search_API_v2)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Restrict results to one ACTIVE category. |
| `near` | query | `string` | no | Place name to geocode, such as City, State, Country. |
| `query` | query | `string` | no | Keywords to search across ACTIVE kids assets. |
| `topicName` | query | `string` | no | Restrict results to one or more topic names. |
