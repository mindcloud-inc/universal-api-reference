# Search Answers with Simplesat

Searches answers in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/answers/search`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Search Answers](https://developer.simplesat.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve |
| `page_size` | query | `number` | no | The number of records per page |
| `start_date` | body | `string` | no | — |
| `end_date` | body | `string` | no | — |
| `operator` | body | `string` | no | — |
| `filters[]` | body | `array<object>` | no | — |
