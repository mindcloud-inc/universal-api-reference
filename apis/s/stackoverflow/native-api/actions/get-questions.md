# Get Questions with Stackoverflow

Retrieves specific questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Questions](https://api.stackexchange.com/docs/questions-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited question IDs to retrieve. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
