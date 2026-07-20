# List Answers with Stackoverflow

Retrieves answers from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/answers`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Answers](https://api.stackexchange.com/docs/answers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
