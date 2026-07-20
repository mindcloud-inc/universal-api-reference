# List Related Questions with Stackoverflow

Retrieves related questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/[:ids]/related`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Related Questions](https://api.stackexchange.com/docs/related-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited question IDs to resolve related questions for. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
