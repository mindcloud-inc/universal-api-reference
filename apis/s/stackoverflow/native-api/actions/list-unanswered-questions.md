# List Unanswered Questions with Stackoverflow

Retrieves questions without answers from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/no-answers`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Unanswered Questions](https://api.stackexchange.com/docs/no-answer-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
