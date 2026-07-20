# List Question Comments with Stackoverflow

Retrieves comments for questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/[:ids]/comments`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Question Comments](https://api.stackexchange.com/docs/comments-on-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited question IDs whose comments to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
