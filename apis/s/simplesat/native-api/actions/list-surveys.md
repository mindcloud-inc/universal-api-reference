# List Surveys with Simplesat

Retrieves surveys from Simplesat.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/surveys`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [List Surveys](https://developer.simplesat.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | The number of surveys to return per page |
| `page` | query | `number` | no | The page number to retrieve. |
