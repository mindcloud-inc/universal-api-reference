# List Question Answers with Stackoverflow

Retrieves answers for questions from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/questions/[:ids]/answers`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Question Answers](https://api.stackexchange.com/docs/answers-on-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-delimited question IDs whose answers to list. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
