# Search Responses with Simplesat

Searches responses in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/responses/search`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Search Responses](https://developer.simplesat.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | The number of responses to return per page |
| `page` | query | `number` | no | The page number to return |
| `start_date` | body | `string` | no | — |
| `created_start_date` | body | `string` | no | — |
| `end_date` | body | `string` | no | — |
| `created_end_date` | body | `string` | no | — |
| `modified_start_date` | body | `string` | no | — |
| `modified_end_date` | body | `string` | no | — |
| `operator` | body | `string` | no | — |
| `filters[]` | body | `array<object>` | no | — |
