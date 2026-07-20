# List Questions with Simplesat

Retrieves questions from Simplesat.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/questions`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [List Questions](https://developer.simplesat.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | query | `number` | no | Filter questions by survey ID |
| `metric` | query | `string` | no | Filter questions by metric |
| `page_size` | query | `number` | no | The number of questions to return per page |
| `page` | query | `number` | no | — |
