# Get Answers with Stackoverflow

Retrieves specific answers from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/answers/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Answers](https://api.stackexchange.com/docs/answers-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-separated Stack Exchange answer IDs. |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
